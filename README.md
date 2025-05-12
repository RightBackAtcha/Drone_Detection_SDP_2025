# Drone Detection, Classification, and Mitigation Using Software-Defined Radios  
![Cal Poly Logo](
**California Polytechnic State University, Pomona**  
**Senior Design Project 2024-2025**

This repository contains the full implementation of a drone detection, classification, and mitigation system leveraging **Software-Defined Radios (SDRs)** and **Machine Learning**. The project explores the use of RF signal analysis to identify drone activity, classify commands, and perform replay attacks for mitigation testing.

![Drone Detection System](images/demo_setup.jpg)

---

## 📡 Overview

The proliferation of drones presents new security challenges. This project provides a proof-of-concept for:

- **Detecting** the presence of drones using RF spectrum monitoring.
- **Classifying** drone commands and behaviors (e.g., idle, move, accelerate).
- **Mitigating** drone threats using replay attacks that exploit communication vulnerabilities.

---

## 🛠️ Features

- 📶 **Signal Acquisition**: Captured drone RF signals using SDRs (e.g., HackRF One).
- 🎵 **Feature Extraction**: Used Mel Frequency Cepstral Coefficients (MFCC) to extract features from raw IQ samples.
- 🤖 **Machine Learning**: Trained Support Vector Machines (SVMs) for drone command classification.
- 🔁 **Replay Attacks**: Implemented RF replay to disrupt or control drone behavior.

---

## 🧪 Methodology

1. **Data Collection**  
   Recorded IQ samples from drones performing various commands using SDR hardware.

2. **Preprocessing**  
   Transformed IQ samples using MFCC for effective machine learning input.

3. **Model Training**  
   Used an SVM classifier to distinguish between drone states like idle, movement, and acceleration.

4. **Replay Attack**  
   Replayed captured RF signals using SDR to emulate drone control commands in real-time.

---

## 📁 Project Structure

<pre>
drone-rf-detection/
├── data/                 # Raw and processed IQ signal files
├── models/               # Trained SVM models
├── src/                  # All source code
│   ├── preprocessing/    # MFCC and signal processing scripts
│   ├── classification/   # SVM training and prediction
│   └── replay/           # Replay attack implementation
├── notebooks/            # Jupyter notebooks for experiments and analysis
├── results/              # Visualizations and evaluation metrics
├── images/               # Diagrams, demo photos, and plots
├── requirements.txt      # Python dependencies
└── README.md             # Project documentation
</pre>

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/drone-rf-detection.git
cd drone-rf-detection
