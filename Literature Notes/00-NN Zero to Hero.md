**Micro grad**
	Neural netoworks under the hood are matamatical functions. Function derivative is very usefull and powerull tool for NN training. They can tell us how we should move/tune network weights to achive better predictions. 
	Example
	L=(ab+c)*f
	e = a*b
	d=c+c
	We want to know how each of the parameters influence the final output L. Derivative can tell us excatly that. When we change some of parameters for a small amount what will be L.
	Back propagation step is the step where we count all the partial derivatives of the fuction and using chani rule we calcculate how the small change of paramaeter will affect the final result. Chanin rule:
	Want dL / dc
    know dL / dd and dd / dc
    chain rule: dL / dc = (dL / dd) * (dd / dc)
If we want to L to go up whe should chnage parameters in the direction of derivatives.
Back propagation thorught the network acctually is applying chain rule backwards though the operations.

Creating neural nets form neurons, neurons are objects which represents math operations w*x+b where x is inputt, w wheight and b bais, often we add some non linear functions to them such as tanh, so neuron would be tanh(w*x+b)
Layer is set of nurons and MPL multi layer perceptron is representation of many layers joined - simple neural net.

Some how we want to messure how good or bad our network for predicting is. We are going to define the loss function, to messure how far from desired output our predicitions are.

Loss is defined as mean squared error function. Form desired output we substract prediction result and square the resulting diff. Ideally we awant to achive 0 loss but that is not possible, we wat to tune the network to make loss as much as posible close to 0.
We are doing backward pass through the the loss, weights are now reciving the gradients, which is telling us if the eg.  sign of gradient is negative if we slightly increse this weight(parameter of neural net) loss will go down. That is desired behaviour of loss, to make it close to 0.
Ahter doing the loss.backward() we should update the parameters, iterate thorough params and update them by small amount in the direction of gradients.

update step change the data, minimize the loss!!!
for p in n.parameters():
    p.data += -0.01*p.grad

Training loop consist of forward pass, actually calclulating the loss, backward pass through the loss and updating the parameters

#TRANING LOOP!!
for k in range(20):
    #forward pass
    ypred=[n(x) for x in xs]
    
    loss_list = [(yout - ygt)**2 for ygt, yout in zip(ys, ypred)] #loss function
    loss=Value(0)
    for elem in loss_list:
        loss+=elem
        
    # backwardpass
    #zero the grads
    for p in n.parameters():
        p.grad=0.0
    
    loss.backward()
    
    #update 
    for p in n.parameters():
        p.data += -0.01*p.grad


**MAKEMORE**

We want to create NN to predict the names, train data set are actual names and we want to develop the system which can predict next character in sequence using several previous characters.
In order to consturct the model we have to implement lookup tables, chars should be mapped to numbers STOI and afterward we will need to extract predictions so we will need inverse operation, ITOS.

For first step we introduced bigram size of 2 and construct counts matrix N (28x28) 26 letters of alphabet and 2 special chars for begin ened end of the word. N is populated by counts of how many times bigram is occured in whole data set.
We should optimez to use only one special char, same for bein and end '.', N is now 27x27

From N we should create probabilities by deviding num of occurences with whole row sum. Multinomial distrubution can be used as an index generator, to make random picks from the data.
Likelihood is product of probabilities, we want it to be as high as possible since we want probabilities close to 1. Since probabilitieas are low we introduce log probabilitieas, if probability is 1 log is 0 and if prob is small number log goes further in negative.
Log likelihood is actually the sum of log probabilities, should be normalized and multiplied by -1 to get negative log likelihood  afterwards we aim for 0, that way our model becomong better.

To implement the model we introduce one hot function, it helps us encode the inputs.
Eg.   .emma STOi will give us [0,5,,13,13,1] that is an input
if we do one hot with size 27, since we have 27 possible chars we will get 5x27 tensor with ones on places where indecies form input occurs
[[1,0,0,0,0,0,...],
 [0,0,0,0,1,0....],
 [1 on index 13],
 [1 on index 13],
 [0,1,0,0,0.....]]
Model construction:
#forward pass
xenc = F.one_hot(xs,num_classes=27).float() # input to the net
logits = xenc @ W #log-counts
counts = logits.exp() #equivalent N
probs = counts / counts.sum(1,keepdims=True)# probabilities for nex char

#define the loss
los = -probs[torch.arange(5),ys].log().mean()  

#update the parameters
W.data += -0.1*W.grad


**MAKEMORE part2 MLP**
Implementing makemore acording to Bengio papper. Firstly we should create embeddings, this can be done just by indexing. Create random matrix 27 x 2 C and embedings could be crated bu C[X] where X are input bigrams, we use 3 char bigram in this example.

creating the model:
since indexing is giving us C[X] dimmension 32x3x2 we want to create model with following data
3 of 2 dimensional embedings. Torch.view is used to help about matrix dimensions

h=torch.tanh(emb.view(emb.shape[0],6) @ W1 + b1)

next layer, output 
27 possible chars for the output and 100 layers as an iput because we had 100 neurons in previous layer

W2=torch.rand(100,27) # 100 inputs form above aboves layer and 27 outs since we have 27 chars
b2 = torch.rand(27)

logits = h @ W2 + b2

counts = logits.exp() #equivalent N
probs = counts / counts.sum(1,keepdims=True)# probabilities for nex char

loss = -prob[torch.arange(32),Y].log().mean()
**loss can be calculated using pytorch, more efficient**
F.cross_entropy(logits,Y)	


Often data set is devided into 3 parts, one for training, around 80%, one for parameter optimization 10% and one for testing 10%. Also due to optimization trainig of net caould be done on batches, radnom samples from traning data set. Learning rate could also be determined, often by experimental method, see which one gives you best performance. Ussually in the begining greater learning rate is performing better and afterward should be reduced to fine tune the net.

#find the best learning rate
lre = torch.linspace(-3,0,1000)
lrs  = 10**lre #10^-3 all till 10^0 with resolution of 1000


for i in range(50000):
    
    #optimization!!!! minibatch construction, tarin net on subsets of data, after creation, intex X an Y with ix
    ix = torch.randint(0,Xtr.shape[0],(32,))
    
    #forward pass
    emb = C[Xtr[ix]] #32x3x2
    h=torch.tanh(emb.view(emb.shape[0],30) @ W1 + b1)
    logits = h @ W2 + b2
    loss = F.cross_entropy(logits,Ytr[ix])
   # print(loss.item())
    #backward pass
    for p in parameters:
        p.grad=None
    loss.backward()
    #update
    #lr=lrs[i]
    lr=0.01
    for p in parameters:
        p.data += -lr*p.grad
        
    #track stats for learning rate
    #lri.append(lre[i])
    stepi.append(i)
    lossi.append(loss.log10().item())


**MAKEMORE part3 Activations Gradients BatchNorm**

First optimization is on logits, for example at the firs iteration we want to hawe equal probabilities for each char to occur next, so we want to minimaze first loss. This can be done by minimizing the weights in logits weights W2, weight in output layer. This can be done by simple multiplication, scaling the weights. eg. W2*=0.01
Also we should be careful about non linear part of out model, we must put most of our data inside active part of tanh function, so we should scle our input weights since tanh is active for numbers near the 0. This also can be done with multiplication W1*=0.2. Those magice number could be deterineted, they are called gains. Gain for tanh is 5/3

Batch normalization techinque
We want to make preactivations to be near the Gaussian, to put all the inputs inside active part of tanh. Preact (hidden layer) neurons can be normalized using hpreact = (hprect - hpreact.mean())/hpreact.std(), so we substract mean and devide by standard deviation. We introduce bngain and bnbias for the BatchNorm layer, those are net parameters and they are trained. This can be done before the trainig, before the forward pass, bnmean and bnstd could be calculated at the END of the training from taning data set!S Since batchnorm layer has its own bias there is no need for biass in layer before.
Residual networks, just chain sequences of
- weight layer - convolution
- batch norm layer
- non linear layer - tanh, relu
Good vizualization example of activations using histogram