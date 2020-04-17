# MTCNN


 What is **Face detection**? and **Face Recognition**? or they are one and the same?
            Detecting a face like structure in an image or a video is called as Face Detection.Not to get confused with face recognition.Face Recognition is classifying a face whether it belongs to a particular human or an animal.
            **Neural Networks** have advanced a lot due to the availability of data these days.Pre-trained models are used in image detection for saving time.
Applications of **Face Detections**
1. Snapchat filter uses face detection
2. Facial Motion capture for designing high-end graphics
3. Auto-focus is feature in modern day cameras which detects faces for proper photographs
4. Lip Reading, where by using facial gestures,we can detect what other person is trying to convey

**Neural Network(NN)** algorithms for facial detection
1. Opencv DLL(Deep Learning Libraries)
2. MTCNN
3. Haar-Cascade and etc

**MTCNN(Multi-task Cascaded Convolutional Network)**
      It's a CNN algorithm where it takes an image, creates it's multiple resolution copies and selects the best one out of them which has the highest kernel score.The following steps are the basic guide towards understanding MTCNN.
1. A 12X12 standard kernel is taken for each copy of image
2. Then the kernel search for a face in each iteration stride by stride(stride is used to reduce time complexity)
3. Problem with moving stride by stride is we have to convert the index values each time to get skipped values of pixels.
4. Small image bigger kernel,Big image smaller kernel is used.The relationship between kernel and the image is inversely proportional.
5. When image is passed to P.Net model, then gives back all bounding boxes with some confidence,this  method is followed for each copy of image.  
6. Then width of bounding boxes are calculated and the boxes which cover maximum area are considered and those with smaller areas are discarded.This method is called NMS(Non Maximum Suppression).
7. Hence by this method boxes with lower confidences are deleted
8. Then the image is re-scaled to it's original Size and the original image is shown.

Source:https://towardsdatascience.com/how-does-a-face-detection-program-work-using-neural-networks-17896df8e6ff

**Opencv DLL**
      OpenCV’s deep learning face detector is based on the Single Shot Detector (SSD) framework with a ResNet base network.It is basically a pre-trained dnn model whish has been trained on of lot of data and images beforehand.The .prototxt file(s) which define the model architecture (i.e., the layers themselves).The .caffemodel file which contains the weights for the actual layers.

**MTCNN Detecting a single face:**
![My friends face](/data/img1.jpg)

**It perfectly detects a single face and it even works good with crowd images:**
![frnds](/data/img2.jpg)


**It detects images of animals like chimpanzees,apes and dogs:**
![output](/data/img3.jpg)


Opencv DLL 
          **detects singles faces and it even correctly detects half faces but lag in detecting face in crowd compared to MTCNN and it only works effciently for low resolution images,**

![Images](/data/img4.jpg)

![Images](/data/img5.jpg)
