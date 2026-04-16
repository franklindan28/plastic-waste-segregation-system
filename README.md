# Plastic Waste Segregation System

## 📌 Overview
This project uses YOLOv8 and microcontroller automation to classify and sort plastic waste (PET, HDPE, PP).

## 🚀 Features
- Real-time object detection using YOLOv8
- Servo-controlled sorting mechanism
- LED indicators for classification

## 🛠️ Tech Stack
- Python
- YOLOv8
- OpenCV
- Arduino
- Jetson Nano

## ⚙️ System Architecture

This system integrates edge AI processing using Jetson Nano with a microcontroller-based control system to automate plastic waste segregation.

### 🔄 Workflow Overview

1. **Image Acquisition**
   - A USB camera connected to the Jetson Nano captures real-time images of incoming plastic waste.

2. **Edge AI Processing (Jetson Nano)**
   - YOLOv8 model performs object detection and classification:
     - PET
     - HDPE
     - PP
     - Unknown
   - The model outputs the detected class with confidence score.

3. **Decision Logic**
   - The Jetson Nano determines the appropriate sorting action based on classification.

4. **Communication Interface**
   - The Jetson Nano sends control signals to the microcontroller via:
     - UART (Serial) / GPIO / USB

5. **Microcontroller Control System**
   - The microcontroller receives commands and handles real-time control:
     - Servo motor actuation
     - Timing and movement coordination

6. **Actuation System**
   - Servo motors perform:
     - Opening mechanism
     - Flap control for sorting
     - Bin rotation

7. **Sensor Feedback**
   - Ultrasonic sensor detects bin capacity
   - Feedback is used to prevent overflow

8. **User Feedback**
   - LED indicators display classification results

---

## 📷 Images
<img src="assets/images/allowed plastic type.jpg" width="500"/>
<img src="assets/images/side view of the machine.jpg" width="500"/>

## 📊 Exploratory Data Analysis Result
<img src="assets/images/P_curve (1).png" width="500"/>
<img src="assets/images/R_curve (1).png" width="500"/>
<img src="assets/images/confusion_matrix_normalized (2).png" width="500"/>
<img src="assets/images/labels (2).jpg" width="500"/>

## 📊 Detection Result using custom model
<img src="assets/images/val_batch0_pred (1).jpg" width="500"/>
<img src="assets/images/val_batch1_pred (1).jpg" width="500"/>

## 📷 Video Demo
[![Watch Demo](assets/images/Screenshot%202026-04-17%20034108.png)](https://www.canva.com/design/DAGXKBWeW9Q/vsMHuxm6JbQ6hHNyjmG0VQ/watch?utm_content=DAGXKBWeW9Q&utm_campaign=designshare&utm_medium=link&utm_source=editor&fbclid=IwY2xjawROEnFleHRuA2FlbQIxMQBicmlkETF0eHJzTGtFbWJvR3FHQUdac3J0YwZhcHBfaWQBMAABHqyMDUwqUg8fL-dHyHp38XLNqB32l9dda2W0hhhvcfGa1LEda2QdqpH1Su1C_aem_Dzm5-V7q7AFO5ma9rgsFtQ)

## 👨‍💻 Author
Franklin D. Dañas Jr

For more details about the system design, implementation, or deployment, feel free to contact me. I’m happy to discuss the project further or collaborate on similar work.