# Drowsiness Detection System

## Overview
This project implements a **Drowsiness Detection System** using **OpenCV** and a Convolutional Neural Network (CNN). The system detects whether a person’s eyes are open or closed, calculates a score based on the state of the eyes, and triggers an alarm if the user is deemed to be drowsy.

## Key Features
- **Real-time Eye Detection**: Uses webcam input to detect eyes and classify their state as "Open" or "Closed".
- **Drowsiness Monitoring**: Continuously monitors the user's eye state and maintains a score to assess drowsiness.
- **Alarm System**: Triggers an audio alarm if drowsiness is detected (i.e., both eyes are closed for an extended period).
- **Image Capture**: Saves a frame of the video feed when the alarm is triggered.

## Technologies Used
- **OpenCV**: For image processing and computer vision tasks.
- **Keras**: For loading the pre-trained CNN model for eye state classification.
- **NumPy**: For numerical operations on arrays.
- **Pygame**: For playing audio alerts.

## Getting Started

### Prerequisites
Make sure you have the following installed:
- Python 3.x
- Required Python libraries:
  - OpenCV
  - Keras
  - NumPy
  - Pygame

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your_username/drowsiness_detection.git
   cd drowsiness_detection

2. Install the required dependencies:
   ```bash
   pip install opencv-python keras numpy pygame

3. Download the Haar Cascade files for face and eye detection and place them in the haar cascade files directory. You can find pre-trained Haar Cascade models online.
4. Download the pre-trained CNN model (cnncat2.h5) and place it in the models directory.
5. Add an alarm sound file (alarm.wav) in the project directory.

### Usage
1. Open the script app.py and set the paths for the Haar Cascade XML files and the CNN model:
   
   ```bash
   face = cv2.CascadeClassifier('haar cascade files/haarcascade_frontalface_alt.xml')
   leye = cv2.CascadeClassifier('haar cascade files/haarcascade_lefteye_2splits.xml')
   reye = cv2.CascadeClassifier('haar cascade files/haarcascade_righteye_2splits.xml')
   model = load_model('models/cnncat2.h5')

2. Run the script:
   ```bash
   python app.py

3. To stop the program, press the 'q' key.

## Output Example
The system will display a video feed from your webcam, showing rectangles around detected faces and eyes. The current score will be displayed at the bottom of the screen. If the score exceeds a threshold indicating drowsiness, an alarm will sound, and a frame will be saved as image.jpg.

## Google Drive Link for this project
https://drive.google.com/file/d/1m2PMRK2JPTpiTgyMLnBU-QewaL9OMoop/view

