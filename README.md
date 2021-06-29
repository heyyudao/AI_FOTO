# AI_FOTO

Hi all, Maureen and I created this machine learning project for one of the Stackable Certificates under NUS-ISS. The project aims to develop a self-organizing photo app using deep learning, supervised learning and signal processing technology. The app's interface is written using PySimpleGUI, and the code can be easily implemented on your computer. We train all the models, and details of the training process will not be discussed here. However, the weights of the model are attached to this repository.

The photo app aims to help users organize their inventory better and reduce problems that arise from digital clutter through facial recognition, emotional detection, blur detection and image category classification.

The final system code can be found in the AI_FOTO.ipynb, where all the different functions of our AI_FOTO app can be found there. 

Function 1 : 
The first function of our app is blur image detection. The AI_FOTO app filters out blurry images and moves the blurred images to a separate folder that the user can delete. The library we are using here is the OpenCV Fast Fourier Transform (FFT) for blur detection in images. Fast Fourier Transform transforms an image to the frequency and spatial domains and subsequently performs classification.

Function 2:
Face detection is a computer vision problem for locating and localizing one or more faces in images. Locating the face refers to finding the face's coordinates, and localization demarcates the face's extent via a bounding box. Here, face detection is performed using the state-of-the-art face detection Multi-task Cascade CNN library. AI_FOTO can quickly filter out images that contain human faces and redirect them to a separate folder for users to view and edit.

Function 3: 
Once we have completed face detection, the image detected can be filtered out and move on to the next step, emotion detection. As there are few available pre-train models available, the AI_FOTO team decided to build our emotion detecting model and evaluate its accuracy based on prediction. The AI@FOTO is looking to classify photos into seven categories based on prediction emotion: happy, sad, angry, scared, disgusted, surprised and contemptuous. 

Function 4: 
The last feature for AI_Foto helps users automatically organize their memories into specific areas of "moments". They can select from 8 common types of interest and have their entire album sorted in the background. The eight categories are animals, architecture, art and culture, food and drinks, landscapes, racing competitions, sports and travel.
We leveraged extracting features from a pre-trained model, MobileNetV3, and inserted a classifier on the top layer. 

Files :
An H5 data file containing all the weights needed for emotion detection (Function 3) 
model_epoch_50_lr0_0001.h5

In the ZIP file Image_Folder, there are several test images that can be used to test our codes. 
Image_Folder
