# AR Glasses with Machine Learning for Real-Time Painting Identification

This project aims to improve the art museum experience by utilizing augmented reality (AR) glasses with machine learning for real-time painting identification and context betterment. The glasses are being developed using Raspberry Pi and use YOLOv3 (You Only Look Once version 3) for object detection and image recognition. This program can detect and identify the painting in real-time, and provide relevant information about the painting and the artist through the AR glasses. 

## Dataset 

The dataset used for this project is the [RoboFlow](https://universe.roboflow.com/capstone-lnujd/painting-recognition) dataset. The dataset at the time only contains 54 images, but more images will be added in the future. The dataset contains 54 images of two different paintings, Mona Lisa and Liberty Leading the People. The dataset is split into 86% training and 8% validation and 2% testing. 

## Installation

To run this project, please follow these steps:

1. Clone the repository: 

        git clone https://github.com/yourusername/yourrepository.git

2. Change the directory to yolov3:

        cd yolov3

3. Install the required packages:

        pip install -r requirements.txt

4. Train the model using the following command:
  
        python train.py --img 640 --batch 16 --epochs 5 --data painting.yaml --weights yolov3.pt

5. The trained model will be saved in the runs/train/exp folder. To test the model on a picture, run the following command:
    
        python detect.py --weights runs/train/exp{# of iteration you want to use}/weights/best.pt --img 640 --conf 0.25 --source painting.jpg

