# Hand-Gesture-Recognition-
A Support Vector Machine (SVM) based Hand Gesture Control System is a machine-learning model that recognizes different hand gestures using images or sensor data. The goal is to allow users to control computers, robots, VR systems, or smart devices without physical controllers—just by using their hand movements.
# 🤖 Real-Time Hand Gesture Recognition using CVZone & TensorFlow

This project uses a webcam to recognize and classify hand gestures in real time. It combines `cvzone` for hand tracking and `TensorFlow/Keras` (trained using Teachable Machine) for gesture classification. It’s a cool application of computer vision and deep learning!

---

## 🧰 Technologies Used

| Tool | Purpose |
|------|---------|
| [cvzone](https://github.com/cvzone/cvzone) | Simplifies OpenCV tasks, used for hand tracking |
| [OpenCV (cv2)](https://opencv.org/) | Real-time video processing |
| [NumPy](https://numpy.org/) | Image matrix manipulation |
| [Teachable Machine](https://teachablemachine.withgoogle.com/) | Easy model training for hand gestures |
| [TensorFlow/Keras](https://www.tensorflow.org/) | Used to load and run the trained model |

---

## 📁 Project Structure

  ```bash
  ├── Model/
  │   ├── keras_model.h5         # Trained model from Teachable Machine
  │   └── labels.txt             # Corresponding labels
  ├── Data/
  │   └── 1/                     # Saved cropped hand images
  ├── dataCollection.py          # Script to collect hand image data
  ├── test.py                    # Script to test real-time classification
  ├── README.md                  # This file
  ```

---

## 🚀 How to Run the Project
  1. Clone the Repository
     ```bash
     git clone https://github.com/yourusername/hand-gesture-recognition.git
     cd hand-gesture-recognition
     ```

  2. Install Dependencies:
     Make sure you have Python 3.7+ and install the required libraries
     ```bash
     pip install cvzone opencv-python numpy tensorflow
     ```
  
  4. python dataCollection.py:
     Collect hand images by pressing s to save
     ```bash
     python dataCollection.py
     ```

  5. Run the Real-Time Classifier:
     This will open the webcam and start predicting
      ```bash
      python test.py
      ```
## 🧠 How It Works
Hand Detection: cvzone.HandTrackingModule detects the hand and returns bounding box coordinates.

Image Preprocessing: The hand region is cropped and resized to a 300x300 white canvas.

Prediction: The cropped image is passed to a pre-trained model using cvzone.ClassificationModule.

Display: The predicted gesture label and confidence score are shown on the webcam feed.

## ✨ Future Improvements
Add more gesture classes

Improve model accuracy by collecting more data

Add voice commands or system control integration

## 📬 Contact
Created with 💙 by Shrey Pandey
