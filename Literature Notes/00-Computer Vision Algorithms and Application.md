**Introduction**:
	1. What is computer vision? 
		1. Field of AI that makes computers understand visual world.
		2. Inverse problem, we try to recover unknowns with insufficient infromation given. We are trying to do the inverse, to describe the world that we see in one or more images and to reconstruct its properties, such as shape, illumination, and color distributions.
		3. We use pyhisic based and probabilistic models
		4. Examples and usage:
			1. OCR
			2. Self driving cars
			3. Machine inspection
			4. Visual indentifiaction

**Image formating**
	1. 2D and 3D space -  ponts, lines, planes - equations
	2. 2D transformations
		![[Pasted image 20221107090659.png]]
	3.3D transformations
	![[Pasted image 20221107090803.png]]
	4. Camera
		1. Distorsion - can be corrected by software
		![[Pasted image 20221107091501.png]]
		2. Ideal camera model - pinhole camera
		3. All camera properties can be described used camera matrix K
		4. Multiple camera usage - image mapping 
	5. Photometric image formation
		![[Pasted image 20221107091931.png]]
	6. Optics
	![[Pasted image 20221107092149.png]]
	7. Digital cameras
	![[Pasted image 20221107092301.png]]
		1.CMOS and CCD senors
		Earlier CCDs are better and CMOS are used for low power devices but todays camera are mostly using CMOS.
	8. Color spaces
		1. RGB
		2. HSV
	9. Optimization and compresion
		1. FFT, DFT -> JPEG 
**Image processing**
	1.Pixel transformations - general definition, takes an input image and produces the output
	2. Color transformations
	3. Histogram equalization
		1. Whole picture histogram 
		2. Blocking histogram equalization technique
		3. locally adaptive algortihm
	4. Linear filtring
		1. Blur / Sharp
	5. Band-pass and stearable filters
		1. Energy
		2. Integral image
		3. Recursive filtering - FIR, IIR
	6. Non-linear filtering
		1. Median filter
	7. Pyramids and wavelets - image blending
8. 
**Deep learning**
	Mainly used for image cassification
**1.Supervised learning**
	![[Pasted image 20221110083818.png]]
		1.Input and labels are fixed, statically trained
		2. model is trained over the large amount of data
		3. Model is used to generate desired outptu from the input data
	**1.1. Data preprocessing**
		1. Apply transformations and prepare traning data
	**1.2. Nearest neighbors**
		1. The training examples are all retained, and at evaluation time the “nearest” k neighbors are found and then averaged to produce the output.
		![[Pasted image 20221110085520.png]]
	**1.3.Support vector machines**
	![[Pasted image 20221110092230.png]]
		Basically finds the border between different samples - maximum margin classifier
		Circled object which are touching dashed lines are called support vectors
	**1.4.Decision trees and forest**
	![[Pasted image 20221110094923.png]]
	2. **Unsupervised learning**
		1. Clustering on various criteria
		2. K-means and Gaussian modles mixture clustering
	3. **Deep neural networks**
		1. Deep neural networks (DNNs) are feedforward computation graphs composed of thousands of simple interconnected “neurons” (units), which, much like logistic regression perform weighted sums of their inputs
		![[Pasted image 20221110132823.png]]
		2. **Activation functions**
		![[Pasted image 20221110133045.png]]
		3.Regularization and normalization
			LASSO
			Data set augmentation -  adding more samples to traning data sets
		    Loss function - minimizing during the traning
		4. Backpropagation
			![[Pasted image 20221114113248.png]]