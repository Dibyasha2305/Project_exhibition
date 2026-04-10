
# SMART CRICKET
An AI-powered system that analyzes cricket batting technique in real-time using computer vision and machine learning.


##  Overview

This project captures live video through a webcam, detects body posture using pose estimation, identifies the cricket shot being played, and provides instant feedback to improve technique.

It acts like a **virtual cricket coach**, helping players refine their stance and movement.



## Features

-  Real-time webcam video capture  
-  Pose detection using MediaPipe (33 body landmarks)  
-  Joint angle calculation (elbow, knee)  
-  Shot classification using Machine Learning  
-  Performance scoring system  
-  Instant corrective feedback  
-  Clean and interactive UI overlay
-  3D Visualisation of a list of forms


##  Tech Stack

- **Python**
- **OpenCV** – Video processing  
- **MediaPipe** – Pose estimation  
- **scikit-learn** – Machine learning (Random Forest)  
- **NumPy / Pandas** – Data processing  
- **Joblib** – Model saving/loading  


##  System Pipeline
Camera → Pose Detection → Keypoints Extraction
→ ML Model (Shot Prediction)
→ Angle Calculation
→ Feedback + Score Display



##  Machine Learning Model

- **Model Used:** Random Forest Classifier  
- **Input:** 33 pose landmarks (x, y, z, visibility → 132 features)  
- **Output:** Cricket shot type  
  - Cover Drive  
  - Pull Shot  
  - Sweep Shot  
  - etc.



##  How It Works

1. Capture live video from webcam  
2. Detect body keypoints using MediaPipe  
3. Predict shot type using trained ML model  
4. Calculate joint angles  
5. Compare with ideal dataset  
6. Generate feedback + score  


##  Example Output

Shot: cover_drive
Elbow: Lower
Knee: OK
Score: 75%
Stance: side_on_stance



##  How to Run

### 1. Clone the repo

```bash
git clone https://github.com/your-username/AI-Cricket-Coach.git
cd AI-Cricket-Coach
```
### 2. Create environment
```bash
conda create -n cricket_env python=3.10
conda activate cricket_env
```
###3. Install dependencies
```bash
pip install opencv-python mediapipe numpy pandas scikit-learn joblib
```
###4.Run the app
```bash
python live_feedback.py
```

##  Project Highlights
Combines Computer Vision + Machine Learning
Real-time performance analysis
Sports-tech application
Scalable and modular design
