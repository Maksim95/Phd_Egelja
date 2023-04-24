# System for detecting driver’s drowsiness, fatigue and inattention
[[System for detecting driver’s drowsiness, fatigue and inattention.pdf]]
*Aleksa Arsic Velibor Ilic Bogdan Pavkovic*
-Advantages: single RGB camera, real time calculations
-Disadvantages: low light conditions, changing light conditions, camera get covered, SAFETY
-Room for improvement: 
	- Introduce more cameras (2 will be sufficient) and implement signal triangulation
	- use NIR cameras for night(changing) light conditions
	- add more variables to monitor driver state eg. HR, gaze direction, spoofing...

# Face Biometric Spoof Detection Method Using a Remote Photoplethysmography Signal
[[Face_Biometric_Spoof_Detection_Method_Using_a_Remo.pdf]]
*Seung-Hyun Kim 1, Su-Min Jeon 1and Eui Chul Lee*
-Advantages: single RGB camera, cheap system, very high accuracy
-Disadvantages: low light conditions, changing light conditions, does not iclulude frot head area fo analysis, SAFETY
-Room for improvement: 
 - make it works in changing ligth condtiotions(aditional model tarining) 
 - maybe introduce thermal camera for beter spoofing detection using body temperature thresholds. Theraml camera can make algorithm more robus and more simple.
 - add more area of face to be involved in calaculations due to make algorithm more robus,

# Remote Pulse Rate Measurement from Near-Infrared Video
[[Remote Pulse Rate Measurement From Near-Infrared Videos.pdf]]
*Sang Bae Park, Gyehyun Kim, Hyun Jae Baek, Jong Hee Han and Joon Ho Kim*
-Advantages: single NIR camera, cheap system, works in low light conditions, high accuracy?, includes filters for noise reduction
-Disadvantages: changing light conditions, safety is not sufficient to be integrated in a car
-Room for improvement: 
	- algorithm optimization to make it more accurate
	- HR to be tracked in real-time with out major delay, since cars are moving fast and few seconds delay could be mandatory
	- integration with more safe systems such as Adaptive AUTOSAR to be deployed in car.

# Camera-based heart rate monitoring in highly dynamic light conditions
[[Camera-based heart rate monitoring in highly dynamic light conditions.pdf]]
*Vincent Jeanne, Michel Asselman, Bert den Brinker, Murtaza Bulut*
-Advantages: single NIR camera, cheap system, works in various light conditions, proven high accuracy
-Disadvantages: car vibrations, camera gets covered, safety is not sufficient to be integrated in a car
-Room for improvement: 
	- add multiple cameras in case one got covered by steering wheel or such...
	- implement signal triangulation between cameras
	- make algorithm more accurate and fast
	- Perform camera stabilizations technique to make it more reliable for car usage

# Driver Monitoring implementation in Adaptive  AUTOSAR environment
[[Driver Monitoring implementation in Adaptive AUTOSAR environment.pdf]]
*Milan Đokić, Stefan Nićetin, Gordana Velikić, Tihomir Anđelić*
-Advantages: single camera, adptive autosar implementation of algorithm
-Disadvantages: drowness detection only, lightnig 
-Room for improvement: 
	- add multiple cameras to make system more robus, 
	- implement signal triangulation
	- optimize algorithm
	- add more variables to track drivers state such as, HR, gaze detection, spoofing...

# Emotionally Adaptive Driver Voice Alert System  for Advanced Driver Assistance System (ADAS)  Applications
[[Emotionally Adaptive Driver Voice Alert System for Advanced Driver Assistance System (ADAS) Applications.pdf]]
*Sarala S M, Sharath Yadav DH, Asadullah Ansari*
-Advantages: adaptive alerts based on driver emotions, 
-Disadvantages: testing only in lab conditions
-Room for improvement: 
	- add multiple cameras to make system more robus, 
	- add NIR cameras for light changing situations
	- add more emotions for classifications, improve NN model
	- combine with other detection algorithms.

# Detection of Emotional States Through the Facial  Expressions of Drivers Embedded in a Portable  System Dedicated to Vehicles
[[Detection of Emotional States Through the Facial Expressions of Drivers Embedded in a Portable System Dedicated to Vehicles.pdf]]
*Eduard Zadobrischi, Lucian-Mihai Cosovanu, Mihai Negru and Mihai Dimian*
-Advantages: emotion detecnio in raw format, could be used for further driver state analysis 
-Disadvantages: safety for car deployment, aditioonal hardware stuff that you have to put in car
-Room for improvement: 
	- make it safety compliatn and deploy in the car 
	- add multiple NIR cameras for light changing situations and triangulation
	- improve NN model
	- combine with other detection algorithms and use emotion detections for futher driver state observations

# Drowsiness Detection Based On Driver Temporal  Behavior Using a New Developed Dataset
[[Drowsiness Detection Based On Driver Temporal Behavior Using a New Developed Dataset.pdf]]
*F. Faraji, F. Lotfi, J. Khorramdel, A. Najafi, A. Ghaffari*
-Advantages: drowness detection using eyes and mouth, rgb camera, multithread approach -> realtime calculations
-Disadvantages: only one camera, changing light conditions
-Room for improvement: 
	- make it safety compliatn and deploy in the car 
	- add multiple NIR cameras for light changing situations and triangulation
	- involve other dorowsiness parameters in calculation such as EEG...
	-further optimeze the algorithm to make it more robus and safe

# Driver Drowsiness Detection Based on Eye Movement and Yawning Using Facial  Landmark Analysis
[[Driver_Drowsiness_Detection_Based_on_Eye.pdf]]
*Anna Liza A. Ramos, Jomar Christian  , Dean Hur T. Mangilaya, Nathaniel Del Carmen, Erika May Enteria, Leonilo Jean Enriquez*
-Advantages: drowness detection using eyes and mouth, single rgb camera(cheap), tested from multiple camera angles
-Disadvantages: changing light conditions, covered camera
-Room for improvement: 
	- better accuracy 
	- Maybe introduce CNNs for image processinf instead of SVM
	- involve other dorowsiness parameters in calculation such as EEG...
	- introduce more cameras and think about changing light condtitions due to RGB camera limitations
	- make it work in realtime

# A Method of Driver’s Eyes Closure and Yawning Detection for Drowsiness Analysis by Infrared Camera
[[A Method of Driver’s Eyes Closure and Yawning Detection for Drowsiness Analysis by Infrared Camera.pdf]]
*Wisaroot Tipprasert, Theekapun Charoenpong, Chamaporn Chianrabutra, Chamaiporn Sukjamsr*
-Advantages: IR camera, able to detect in low-light conditions,
-Disadvantages: covered camera, error prone
-Room for improvement: 
	- better accuracy 
	- Maybe introduce CNNs for image processinf instead of SVM
	- involve other dorowsiness parameters in calculation such as EEG...
	- introduce more cameras, maybe combine differnet types of cameras

# Face Key Point Location Method based on Parallel Convolutional Neural Network
[[Face Key Point Location Method based on Parallel Convolutional Neural Network.pdf]]
*Zhou Pu, Kai Wang, Kai Yan*
-Advantages: parallel CNN approach, could be used for further face analysis
-Disadvantages: not tested on video
-Room for improvement: 
	- better accuracy 
	- could be used as face detector for driver monitoring systems

# A Comprehensive Study on Upper-Body Detection with Deep Neural Networks
[[A Comprehensive Study on Upper-Body Detection with Deep Neural Networks.pdf]]
*Yamei Zhu, Lin Zhang*
-Advantages: analysis of differnet approaches for pedestrian detection CNN, R-CNN, YOLOv2
-Disadvantages: not related to driver observation but usefull for ADAS applications
-Room for improvement: 
	- analyze on video
	- more detailed approach for driver and cabin obseravtion

# Multi-Level Classification of Driver Drowsiness by Simultaneous Analysis of ECG and Respiration Signals Using Deep Neural Networks
[[Multi-Level Classification of Driver Drowsiness by Simultaneous Analysis of ECG and Respiration Signals Using Deep Neural Networks.pdf]]
*Ebrahimian, S., Nahvi, A., Tashakori, M., Salmanzadeh, H., Mohseni, O., & Leppänen, T.*
-Advantages: usage of thermal camera, reliable testing, usage of respiration to monitor the drviver state, VERY NICE TECHNICAL DESCRIPTIONS!!!
-Disadvantages: bit lower accuracy
-Room for improvement: 
	- improve accuracy 
	- add more sensors to drivers seat, seering wheel to mesure driver state variables

# A Comparative Analysis of using Various Machine learning Techniques based on Drowsy Driver Detection
[[A Comparative Analysis of using Various Machine learning Techniques based on Drowsy Driver Detection.pdf]]
*A Bano, A Saxena, G K Das*
-Advantages: Nice example of overview papper!
-Disadvantages:
-Room for improvement: 


# 4D: A Real-Time Driver Drowsiness Detector Using Deep Learning
[[4D A Real-Time Driver Drowsiness Detector Using Deep Learning.pdf]]
*Jahan, Israt and Uddin, K. M. Aslam and Murad, Saydul Akbar and Miah, M. Saef Ullah and Khan, Tanvir Zaman and Masud, Mehedi and Aljahdali, Sultan and Bairagi, Anupam Kumar*
-Advantages: nice comparison with other pappers
-Disadvantages: eye images only
-Room for improvement: 
	- add more variables to driver state calculation such as HR, mouth, gaze, yawning...
	- test it on video, maybe improve efficiency to work in realtime videos
	- improve accuracy
	- involve multiple cameras
# Real Time Driver Fatigue Detection System Based on Multi-Task ConNN
[[Real Time Driver Fatigue Detection System Based on Multi-Task ConNN.pdf]]
*Kir Savas, Yasar Becerkli*
-Advantages: nice comparison with other pappers in introduction, interesting one is nose tracking with Kalman and Track-Learning-Detection
-Disadvantages: eye PERCLOS and mouth for yawning only, single camera, rgb camera
-Room for improvement: 
	- add more variables to driver state calculation such as HR, gaze, respiration
	- involve multiple cameras
	- could be usefu as par of driver monitoring system in Interior perception

# Driver Behavior Recognition via Interwoven  Deep Convolutional Neural Nets With Multi-Stream Inputs
[[Driver Behavior Recognition via Interwoven Deep Convolutional Neural Nets With Multi-Stream Inputs.pdf]]
*CHAOYUN ZHANG, RUI LI, WOOJIN KIM, DAESUB YOON AND PAUL PATRAS*
-Advantages: two cameras, mocked testing environmet to emulate car conditions in lab, realtime calculations, fair accuracy, combination of classic and deep learning computer vision, interesting driver actions detected such as, texting, eating, gaming, drinking.... nice techincal descriptions
-Disadvantages: rgb cameras only
-Room for improvement: 
	- make it work in changing light conditions -> NIR camera
	- driver position triangulation if one of camera gets covered
	- maybe add some more sensors and enacapsulate it to driver monitor system

# Driver Drowsiness Detection
[[Driver Drowsiness Detection.pdf]]
*K.Satish, A.Lalitesh, K. Bhargavi, M.Sishir Prem and Anjali.T*
-Advantages: two factor drowsiness detection, eyes and hand pressure to seering wheel, raltime calculations
-Disadvantages: accuracy, single camera, not working in vrious light conditions, 
-Room for improvement: 
	- make it work in changing light conditions -> NIR camera
	- driver position triangulation if one of camera gets covered
	- make computer vision algorithm more robus
	- add more factors beside blink rate to drowsiness calculation

# Appearance-Based Gaze Tracking Through Supervised Machine Learning
[[Appearance-Based Gaze Tracking Through Supervised Machine Learning.pdf]]
*Daniel Melesse, Mahmoud Khalil, Elias Kagabo, Taikang Ning, and Kevin Huang*
-Advantages: Cheap computing power Viola Jones detection algorithm, low cost, single RGB(web) camera
-Disadvantages: less accuaracy due to Viola Jones usage, not working on video, not working in realtime
-Room for improvement: 
	- Introduce more robus CNN for face region detection
	- make it work in realtime
	- use 2 NIR cameras, IR light is very good due to reflection from human eye

# Free-Head Appearance-Based Eye Gaze Estimation on Mobile Devices
[[Free-Head Appearance-Based Eye Gaze Estimation on Mobile Devices.pdf]]
*Liu Jigang, Bu Sung Lee, Deepu Rajan*
-Advantages: device builtin camera usage, very high accuracy, niece theoretical explanation of gaze estimation process, reliable detections
-Disadvantages: realtime calculation not mentioned
-Room for improvement: 
	- use NIR camera for car ussage, it may also improve accuarcy
	- make it work in realtime ?
	- nice to use it as a part of driver observation system 

# Implementation of Human Face and Spoofing Detection Using Deep Learning on Embedded Hardware
[[Implementation of Human Face and Spoofing Detection Using Deep Learning on Embedded Hardware.pdf]]
*Saankhya Mondal*
-Advantages: high accuracy, vorking on video, cheap RGB(web camera)
-Disadvantages: not involving HR, or eye movement..., most testing done on pictures
-Room for improvement: 
	- improve accuracy by involving other methods for spoofing detection
	- test in various light conditions
	- maybe intrdouce second camera for car application since at some time points single camera could be covered

# Comparison of the Deep Learning Methods Applied on Human Eye Detection
[[Comparison of the Deep Learning Methods Applied on Human Eye Detection.pdf]]
*Yunjie Xiang, Haiyan Yang, Rong Hu, Chih-Yu Hsu*
-Advantages: nice overview of the field, comparison of YOLOv3 and fast RCNN(Res-Net50) algorithms for direct eye detection
-Disadvantages: none, sice is just explaining comparison between two algorithms
-Room for improvement: 
	- face detectors are now more advanced, they can detect face with mask

# Improvement of Face and Eye Detection  Performance by Using Multi-task Cascaded  Convolutional Networks
[[Improvement of Face and Eye Detection Performance by Using Multi-task Cascaded Convolutional Networks.pdf]]
*Mahmudul Hasan Robin, Md. Minhaz Ur Rahman, Abu Mohammad Taief and Ms. Qamrun Nahar Eity*
-Advantages: high accuaracy, relatively simple system, nice comparison to other techniques
-Disadvantages: RGB camera only, controlled light conditions
-Room for improvement: 
	- test it under various light conditions
	- maybe improve preprocessing
	- try to make it work with direct eye detection, without face

# Driver Distraction Detection and Identity Recognition in Real-time
[[Driver Distraction Detection and Identity Recognition in Real-Time.pdf]]
*Jinhua Zeng, Yaoru Sun, Li Jiang*
-Advantages: attention budget strategy, changing light conditions
-Disadvantages: face and eyes only, gaze etimation using head orientation, not eyes
-Room for improvement: 
	- add more variables to check driver distraction rg. speeking, phone usage recognition...
	- implement real gaze estimator, based on eye tracking, not head only
	- more sophisticated "real" testing

# Detection of Distracted Driver using Convolutional Neural Network
[[Detection of Distracted Driver using Convolutional Neural Network.pdf]]
*Bhakti Baheti, Suhas Gajre, Sanjay Talbar*
-Advantages: VGG-16 architecture optimization wth nearly same accuracy, NICE usage manual distraction cues, NICE net and techniques used descriptions!
-Disadvantages: malual cues only, single camera, changing light condtiotions
-Room for improvement: 
	- add more facial cues to distraction analysis, eg. eyes
	- add speech recognition

# Real-Time Driver Gaze Direction Detection Using the 3D Triangle Model and Neural Networks
[[Real-Time Driver Gaze Direction Detection Using the 3D Triangle Model and Neural Networks.pdf]]
*Wen-Chang Cheng, You-Song Xu*
-Advantages: 2 cameras, trinagulation, fair accuracy, can run in real time, 3D triangle ALGORITHM: eyes and middle of the lips are vertices for triange, when triangle brakes orientation => has been changed
-Disadvantages: gaze detection only, changing liht conditions
-Room for improvement: 
	- could be used as a prat of more sophisticated system for driver monitoring

# Two Stream Deep Convolutional Neural Network for Eye State Recognition and Blink Detection
[[Two Stream Deep Convolutional Neural Network for Eye State Recognition and Blink Detection.pdf]]
*Ritabrata Sanyal, Kunal Chakrabarty*
-Advantages: good accuracy on eye detection and state recognition, NICE data sets for traning and testing are proposed, paralell RGB and binary mask blink detectors -> better accuracy, nice descriptions of the system
-Disadvantages: not tested in changing light conditions
-Room for improvement: 
	- could be used as a part of driver observation system
	- make it run in realtime -> improve the performance

# EYE GAZE TRACKING BASED DRIVER MONITORING SYSTEM
[[Eye gaze tracking based driver monitoring system.pdf]]
Annu George Mavely , J.E Judith2 ,Sahal P A , Steffy Ann Kuruvilla
-Advantages: works on RospberyPi, nice algorithm explanation and schema
-Disadvantages: actually nothing ralted to gaze, similar thing like Aleksa developed just without NN
-Room for improvement: 
	- try to track actual eye gaze of the driver 


# Face Spoof Detection by Motion Analysis on the Whole Video Frames
[[Face Spoof Detection by Motion Analysis on the Whole Video Frames.pdf]]
Heni Endah Utami, Hertog Nugroho
-Advantages: different approach, good accuracy, background analysis, nice comparison with other researches
-Disadvantages: tested/works ony in lab environmet
-Room for improvement: 
	- try with IR cam
	- tetst it in car

# Deep Learning based Face Liveness Detection in Videos
[[Deep Learning based Face Liveness Detection in Videos.pdf]]
Y. Akbulut, A. Şengür, Ü. Budak and S. Ekici
-Advantages: NN approach, comparison between different NN achitectures, tested on many examples
-Disadvantages: no clear algorithm, fair accuracy
-Room for improvement: 
	- real world testing
	- find key features which are necessary to detect livness in human face


# Cepstral Based Heart Rate Estimation
[[Cepstral Based Heart Rate Estimation.pdf]]
Milan Milivojeviü, Ana Gavrovska,Marijeta Slavkoviü-Iliü, Irini Reljin
-Advantages: similar techniques could be applied to rPPG
-Disadvantages: contact based approach
-Room for improvement: 
	- contact less solution
	- IR camera

# Color Spaces and Regions of Interest in Camera Based Heart Rate Estimation
[[Color Spaces and Regions of Interest in Camera Based.pdf]]
Hannes Ernst, Matthieu Scherpf, Hagen Malberg, and Martin Schmidt
-Advantages: nice comparioson between different ROIs on the face
-Disadvantages: 
-Room for improvement: 
	- could be useful for future work spoofing, HR estimation

# Real-time Drowsiness Detection Algorithm for Driver State Monitoring Systems
[[Real-time Drowsiness Detection Algorithm for Driver State Monitoring Systems.pdf]]
Jang Woon Baek, Byung-Gil Han, Kwang-Ju Kim, Yun-Su Chung, Soo-In Lee
-Advantages: works on embedded device, IR camera, very simple algorithm, NN for face detection
-Disadvantages: eye state monitoring only
-Room for improvement: 
	- include HR in calculations, driver activity...

# Hybrid driver monitoring system based on Internet of Things and machine learning
[[Hybrid driver monitoring system based on Internet of.pdf]]
Lian Zhu,Yijing Xiao, Xiang Li
-Advantages: Hybrid approach, data collection from phones, werable devices, nice overview of the field
-Disadvantages: Large ammount of data to be analyzed, could be easily "hacked" in terms of getting "fake" data from phone, werble devices... proposal only, no implementatio, just a brief idea
-Room for improvement: 
	- try to implement such a system
	- make data obtaoined from various devices more reliable

# Camera-based Driver Drowsiness State  Classification Using Logistic Regression Models
Mercedes-Benz AG
[[Camera-based Driver Drowsiness State.pdf]]
Mohamed Hedi Baccour, Frauke Driewer, Tim Sch ̈ack, Enkelejda Kasneci
-Advantages: nice exoplanation of drowsiness parameters, suggestions to use other parameteres like ego vehicle distance to center line, steering whell angle
-Disadvantages: eyes and head orientation only
-Room for improvement: 
	- involve other drowsiness parameters in calculations
	- maybe introduce observation of keep lane system interventions, too many or too stiff intervention tells us that driver is drowsy