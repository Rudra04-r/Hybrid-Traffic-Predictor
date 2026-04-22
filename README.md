# Hybrid-Traffic-Predictor
# 🚦 Hybrid LSTM-GRU for Short-Term Traffic Flow Prediction

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![Keras](https://img.shields.io/badge/Keras-API-red)
![License](https://img.shields.io/badge/License-MIT-green)

## 📌 Overview
Accurate short-term traffic flow prediction is a critical component of modern Intelligent Transportation Systems (ITS). This repository contains the code and methodology for a **Hybrid LSTM-GRU deep learning architecture** designed to forecast traffic volume in real-time. 

By combining the long-term memory retention of Long Short-Term Memory (LSTM) networks with the computational efficiency and rapid updating of Gated Recurrent Units (GRU), this model effectively captures the highly non-linear spatio-temporal dependencies of urban traffic.

📄 **Read the full research paper:** [Traffic_Prediction_Research_Paper.pdf](./Traffic_Prediction_Research_Paper.pdf)

## ✨ Key Features
- **Stacked Architecture:** Feeds complex, long-term features from an LSTM layer into a rapid, responsive GRU layer.
- **Multi-Step Forecasting:** Evaluated across 15-minute, 30-minute, and 60-minute prediction horizons.
- **Peak Hour Robustness:** Specifically tested to handle extreme volatility during morning commutes and rush hours.
- **Benchmarked:** Outperforms standalone LSTM and GRU models in both RMSE and MAE.

## 📊 Dataset (PEMS08)
This project utilizes the **PEMS08** dataset, collected by the California Department of Transportation (Caltrans) Performance Measurement System (PeMS).
- **Time Span:** 62 days (July - August 2016)
- **Nodes:** 170 independent sensor stations
- **Resolution:** 5-minute intervals
- **Features:** Traffic Flow (Volume), Occupancy, Average Speed

## 🧠 Model Architecture
The data is processed using a sliding window approach, normalized via Min-Max scaling, and fed into the following architecture:
1. **Input Layer:** Historical traffic sequence.
2. **LSTM Layer:** Extracts deep, long-term historical trends.
3. **Dropout Layer (0.2):** Prevents overfitting.
4. **GRU Layer:** Captures short-term, immediate traffic fluctuations.
5. **Dense Layer:** Outputs the continuous flow prediction.

*(Optional: Add your architecture diagram here)*
> `![Architecture Diagram](link-to-your-diagram-image.png)`

## 🚀 Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/yourusername/Hybrid-Traffic-Predictor.git](https://github.com/yourusername/Hybrid-Traffic-Predictor.git)
   cd Hybrid-Traffic-Predictor
