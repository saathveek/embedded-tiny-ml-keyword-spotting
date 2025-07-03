![Project Banner](assets/github_banner_tiny_ml.png)

# Embedded Keyword Spotting with Tiny Machine Learning

[![View Code](https://img.shields.io/badge/View-Repository-blue)](https://github.com/saathveek/embedded-tiny-ml-keyword-spotting)  
![Python 3.10+](https://img.shields.io/badge/Python-3.10%2B-blue.svg)
![Jupyter Notebook](https://img.shields.io/badge/Notebook-Jupyter-orange.svg)  
![Arduino Nano 33 BLE Sense](https://img.shields.io/badge/Board-Arduino%20Nano%2033%20BLE%20Sense-teal.svg)  
![TensorFlow Lite](https://img.shields.io/badge/TensorFlow-Lite-orange.svg)  
[![MIT License](https://img.shields.io/badge/Software%20License-MIT-blue.svg)](LICENSE)
[![Data License: CC BY-NC 4.0](https://img.shields.io/badge/Data%20License-CC--BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)

This project implements a continuous keyword spotting system using Tiny Machine Learning techniques deployed on the **Arduino Nano 33 BLE Sense**.

## Project Overview

We developed a real-time wake-word detection model capable of running on ultra-low-power hardware using **TensorFlow Lite for Microcontrollers**. The system listens continuously and responds when a specific keyword is spoken — enabling voice-activated interfaces on edge devices without needing cloud connectivity.

## Motivation

Traditional keyword detection systems rely on cloud processing or powerful edge hardware. TinyML offers the opportunity to bring machine learning to power-constrained, real-world environments like wearable devices, environmental sensors, or assistive technologies — all while maintaining privacy and real-time performance.

## Methods

- **Hardware**:  
  - Arduino Nano 33 BLE Sense  
  - Onboard microphone and IMU  

- **Data**:  
  - Custom-recorded and preprocessed keyword audio samples  
  - Background noise samples for training robustness

- **Model Architecture**:  
  - Preprocessing pipeline: Windowing → FFT → Spectrogram  
  - Lightweight CNN architecture with quantization for deployment  

- **Workflow**:  
  - Data preprocessing using Python  
  - Model training and evaluation using TensorFlow  
  - Conversion to `.tflite` and deployment with `TensorFlow Lite Micro`  
  - Live testing using Arduino IDE and serial monitor

## Key Features

- Real-time audio classification directly on microcontroller  
- Optimized for low memory (RAM/Flash) constraints  
- Handles background noise and avoids false positives  

## Results

- Achieved over 90% accuracy for binary classification (keyword vs. background)  
- Inference time < ___ms  
- Total model size < ___KB  

## Repo Structure

- `model/`: TensorFlow training scripts and `.tflite` export  
- `arduino/`: Arduino sketch for embedded inference  
- `data/`: Audio data for training and testing  
- `notebooks/`: Jupyter notebooks for EDA and prototyping  
- `docs/`: Visuals and diagrams for system architecture

## Tech Stack

- Python  
- TensorFlow & TensorFlow Lite  
- Arduino C++  
- Jupyter Notebooks  

## Getting Started

1. Clone the repo  
2. Install Python dependencies: `pip install -r requirements.txt`  
3. Train and convert the model with scripts in the `model/` folder  
4. Open the Arduino sketch in `arduino/` and upload it to the board  
5. Say your keyword and watch the serial monitor react in real time!

## License

This project is licensed under the [MIT License](LICENSE).

## Author

**Saathveek Gowrishankar**  
Embedded ML Researcher | UIUC  
[saathveek.com](https://saathveek.com)  
[LinkedIn](https://linkedin.com/in/saathveek)  
[gsaathveek@gmail.com](mailto:gsaathveek@gmail.com)

## Contact

Want to collaborate or ask questions? Reach out via [email](mailto:gsaathveek@gmail.com) or [LinkedIn](https://linkedin.com/in/saathveek).
