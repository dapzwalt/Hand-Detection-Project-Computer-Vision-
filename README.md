# Hand-Detection-Project-Computer-Vision-

![image](https://github.com/dapzwalt/Hand-Detection-Project-Computer-Vision-/assets/125368548/83f84c11-41a0-41b1-986e-d712a63dee7a)

## Hand Detection with MediaPipe

## Table of Contents
- [Overview](#overview)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [Sample Output](sample-output)
- [Contributions](#contributions)
- [License](#license)

## Overview
Hand detection using computer vision is a fundamental task in the fields of computer vision and human-computer interaction. It involves identifying and localizing human hands 
within an image or video stream. Hand detection can be used in various applications, including gesture recognition, sign language interpretation, hand tracking in virtual reality,
and human-computer interaction. We leveraged computer vision to identify and track hands in real-time using my webcam. This project illustrates the use of MediaPipe as well as the OpenCV library.

## Project Structure
- Importing Necessary libraries: I imported two very important libraries for this project, which are OpenCV and MediaPipe
- Identification Of Webcam: It then identifies your webcam, either an inbuilt one or an external one.
- Processing of Image: The code we use helps to switch your webcam and converts the image from BGR to RGB required for MediaPipe
- Hand Detection with MediaPipe: The mediaPipe library tracks and detects hand landmarks. The detected landmark are then visualized on the screen

## Usage
 Hand detection using the MediaPipe library is a powerful and straightforward process.

### Install and Import MediaPipe
First, you need to install the MediaPipe library using pip.
> *pip install mediapipe*
Then, import it into your Python code:
> *import mediaPipe as mp*

### Initialize the Hand Module 
MediaPipe provides a pre-trained hand module that you can easily use.
> *mp_hands = mp.solutions.hands*
> *hands = mp_hands.Hands()*

### Capture Video Stream or Load Image 
You can either capture a live video stream from a camera or load an image in which you want to detect hands. If you're working with a video stream, you can use OpenCV to access the camera feed.

### Process the Frames 
Loop through the frames of the video or process the image to perform hand detection.
> *while True:  # If processing a video stream
         # Read a frame from the video stream or load an image
         # Convert the frame to RGB
         # Perform hand detection
         results = hands.process(frame_rgb)
         if results.multi_hand_landmarks:
             # Extract hand landmarks
             for hand_landmarks in results.multi_hand_landmarks:
                 # Process the landmarks as needed*

### Accessing Landmarks 
MediaPipe provides landmarks for each detected hand, which are 21 points on each hand.
> *for landmark in hand_landmarks.landmark:
    x = landmark.x  # X-coordinate of the landmark
    y = landmark.y  # Y-coordinate of the landmark
    z = landmark.z  # Z-coordinate of the landmark*

### Visualize the Results 
You can use OpenCV or other libraries to draw landmarks or bounding boxes around the detected hands for visualization.

## Sample Output
Here are some examples of the project's output:

![HD1](https://github.com/dapzwalt/Hand-Detection-Project-Computer-Vision-/assets/125368548/c5c2f26c-84b8-47a7-bdad-a305782b4e53)
![HD3](https://github.com/dapzwalt/Hand-Detection-Project-Computer-Vision-/assets/125368548/e5576ce6-21dc-49bf-a27a-4aaa74f76d7a)
![HD4](https://github.com/dapzwalt/Hand-Detection-Project-Computer-Vision-/assets/125368548/f7d61a21-0a86-48d1-8625-0e7f26b3ffcc)

## Contributions
Please drop your contributions here on how to improve this work or give additional input for further learning.

## License
MediaPipe is an open-source framework developed by Google and available under the MIT license, that provides a wide range of computer vision and machine learning solutions, including hand detection.



