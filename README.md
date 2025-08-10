# Sign-Language-Translator

###📜 Overview
Over 1.5 billion people — nearly 20% of the global population — live with hearing loss.
For millions, sign language is the primary mode of communication.

This project aims to enable deaf and mute individuals to communicate more conveniently by recognizing sign language gestures using computer vision and deep learning.

Our approach combines hand landmark detection with sequence-based modeling to classify gestures accurately, even for signs requiring motion.

###🎯 Goals
- Capture all 26 letters of the sign language alphabet.
- Handle static gestures and motion-based gestures (e.g., J, Z).
- Deliver a robust gesture recognition pipeline that works in real time.

###📂 Dataset Preparation
1. Data Collection
  Images collected manually using a webcam(26 letters of the alphabet).


2. Data Preprocessing
2.1 Hand Landmark Detection via MediaPipe

- Hand Detection Model → Generates an oriented bounding box around the detected hand.
- Hand Landmark Model → Extracts 21 high-fidelity 3D keypoints from the detected hand.

2.2 Normalization
All landmark coordinates are normalized to a range of [0.0, 1.0],
based on the image’s width and height.



3️. Labeling
Each gesture sequence assigned a label → the letter it represents.

### 🧠 Models
#### LSTM

- Processes temporal sequences instead of single frames.
- Captures gesture dynamics across time.
- Handles variations in tempo and amplitude of gestures.
- Predicts gesture class from movement patterns.



### RandomForestClassifier
Serves as a baseline model for classification using extracted features, working with moving gestures letters.
