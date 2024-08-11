# Driver-Drowsiness-Alert-System

## 🔧 Technologies & Tools

[![Tools](https://skillicons.dev/icons?i=python,anaconda,github,&perline=20)](https://skillicons.dev)

## Overview
The Driver Drowsiness Alert System is designed to monitor a driver's eye movements and detect signs of drowsiness in real-time. The system uses computer vision techniques to analyze the driver's eye state (open or closed) and triggers an alert if the eyes remain closed for an extended period, indicating potential drowsiness.

## Features
- **Real-Time Eye Detection**: The system uses a pre-trained Haar Cascade classifier to detect eyes from the webcam feed.
- **Eye State Classification**: The model classifies the eye state as open or closed using a convolutional neural network (CNN) with sigmoid activation.
- **Alert System**: An audible alarm is triggered if the eyes remain closed for more than a specified duration, indicating that the driver might be drowsy.
- **Dynamic Video Capture**: Automatically adjusts to different webcams and their respective indices.
- **User-Friendly Interface**: Displays the status of the driver's eyes (open or closed) and provides visual feedback with a text overlay on the video feed.

## Prerequisites
- Python 3.x
- OpenCV
- TensorFlow or Keras (for the neural network model)
- Numpy
- Other dependencies can be installed via the `requirements.txt` file.

## Installation
1. Clone the repository:
git clone https://github.com/benduBytes/Driver-Drowsiness-Alert-System
2. Install the required packages:
pip install -r requirements.txt

## Running the Project
1. **Prepare the Dataset:**
- Ensure that the Haar Cascade files for eye detection (`haarcascade_eye.xml`) are available in the `src/` directory.
- Use the provided Jupyter notebook in the `src/projectCodeFile/` directory for training or modifying the eye state detection model.
2. **Run the Live Demo:**
- Start the webcam feed and perform real-time drowsiness detection:
  ```
  python src/driver_drowsiness.py
  ```
- The system will begin detecting your eyes, displaying whether they are open or closed, and will trigger an alarm if drowsiness is detected.

## Directory Structure
- **`data/`**: Contains datasets.
- **`docs/`**: Includes project documentation, presentations, and reports.
- **`notebooks/`**: Jupyter notebooks, including those saved in HTML format.
- **`results/`**: Stores output results in the form of media.
- **`src/`**: The source code for the project, including the main driver drowsiness detection script.

## Model Details
- **Architecture**: The neural network uses a CNN architecture with a sigmoid activation function for binary classification of the eye state.
- **Training**: The model should be trained on a dataset with labeled images of open and closed eyes, ensuring a balance between the classes.
- **Prediction**: The model outputs a probability for the eye state, which is used to determine whether the eyes are open or closed.

## Example Output
- When the eyes are detected as open, the system displays "Active" with a green text overlay.
- When the eyes are detected as closed for an extended period, the system triggers a sleep alert with a red text overlay and sounds an alarm.

## Customization
- You can adjust the sensitivity of the drowsiness detection by modifying the duration threshold in the code.
- The alarm frequency and duration can also be customized to suit your preferences.

## Issues and Improvements
- The system's accuracy may vary depending on the lighting conditions and the quality of the webcam.
- Future improvements could include integrating more advanced deep learning models and optimizing the eye detection process.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any enhancements, bug fixes, or new features.
