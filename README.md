# Drone Detection, Classification, and Mitigation Using Software-Defined Radios  

![Cal Poly Logo](CPP_Horizontal_2C_Green_RGB-700px.png)

**California Polytechnic State University, Pomona**  
**Senior Design Project 2024-2025**

This repository contains the full implementation of a drone detection, classification, and mitigation system leveraging **Software-Defined Radios (SDRs)** and **Machine Learning**. The project explores the use of RF signal analysis to identify drone activity, classify commands, and perform replay attacks for mitigation testing.

![Drone Detection System](images/demo_setup.jpg)

---

## Overview

The proliferation of drones presents new security challenges. This project provides a proof-of-concept for:

- **Detecting** the presence of drones using RF spectrum monitoring.
- **Classifying** drone commands and behaviors (e.g., idle, move, accelerate).
- **Mitigating** drone threats using replay attacks that exploit communication vulnerabilities.

---

## Features

- 📶 **Signal Acquisition**: Captured drone RF signals using SDRs (e.g., HackRF One).
- 🎵 **Feature Extraction**: Used Mel Frequency Cepstral Coefficients (MFCC) to extract features from raw IQ samples.
- 🤖 **Machine Learning**: Trained Support Vector Machines (SVMs) for drone command classification.
- 🔁 **Replay Attacks**: Implemented RF replay to disrupt or control drone behavior.

---

## Methodology

1. **Data Collection**  
   Recorded RF signal samples from drones performing various commands using SDR hardware.

2. **Preprocessing**  
   Extracted MFCC features from sampled signals for machine learning classification.

3. **Model Training**  
   Used an SVM classifier to distinguish between drone models based on their MFCC features.

4. **Replay Attack**  
   Replayes drone-landing RF signals from dataset to force classified drone to land.
