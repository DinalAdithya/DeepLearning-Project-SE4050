# Battery Capacity Prediction using Deep Learning

## 📋 Project Overview
This project implements and compares deep learning models for predicting lithium-ion battery capacity degradation using historical capacity data. Developed as part of SE4050 Deep Learning course assignment.

## 👥 Team Members
| Role | Name | Student ID | Responsibilities |
|------|------|------------|------------------|
| Group Leader | Adithya D | IT21330278 | Data Visualization, Dense Model, CNN Model, Evaluation, Report |
| Member 2 | Denuwan P.M.K | IT22229434 | LSTM Model Implementation |
| Member 3 | Deshan P.H.P | IT22552556 | GRU Model Implementation |
| Member 4 | Vithana D.T.M | IT22150998 | Data Analysis & Report Support |

## 🎯 Problem Statement
Predict future battery capacity values based on historical capacity measurements to monitor State of Health (SOH) and enable proactive maintenance for lithium-ion batteries.

## 📊 Dataset
We use the **NASA Battery Dataset** which contains run-to-failure battery cycling data.

- **Source**: [NASA Prognostics Center of Excellence](https://www.nasa.gov/intelligent-systems-division/discovery-and-systems-health/pcoe/pcoe-data-set-repository/)
- **Download**: [Battery Data Set](https://phm-datasets.s3.amazonaws.com/NASA/5.+Battery+Data+Set.zip)
- **Citation**: Saha, B., & Goebel, K. (2007). Battery Data Set, NASA Ames Prognostics Data Repository
- **Features Used**: Capacity measurements over charge/discharge cycles
- **Target**: Future capacity values (regression task)

## 🏗️ Models Implemented

### 1. Dense Neural Network (Baseline)
- Simple feed-forward neural network
- Linear regression approach for stable performance
- Serves as performance benchmark

### 2. Convolutional Neural Network (CNN)
- 1D CNN for sequence pattern recognition
- CNN-Linear hybrid approach for stability
- Local temporal feature extraction

### 3. Long Short-Term Memory (LSTM)
- LSTM architecture for long-term sequence learning
- Captures temporal dependencies in battery degradation
- Ideal for time series forecasting

### 4. Gated Recurrent Unit (GRU)
- GRU network implementation for time series
- Efficient alternative to LSTM
- Temporal pattern learning

## 📈 Results Summary

| Model | Test MAE | Test R² | Training Time | Key Finding |
|-------|----------|---------|---------------|-------------|
| **Dense Network** | **0.0175** | **0.8019** | Fast | **Best overall performance** |
| **CNN** | 0.0187 | 0.2138 | Medium | Good pattern recognition |
| **LSTM** | [Pending] | [Pending] | Slow | Expected best for sequences |
| **GRU** | [Pending] | [Pending] | Medium | Expected efficient alternative |

## 🔍 Key Insights
- **Simple models can be highly effective** for battery capacity prediction
- **Proper data preprocessing** is crucial for time series prediction
- **Multiple evaluation metrics** provide comprehensive model assessment
- **Linear patterns dominate** in battery degradation data

## 🛠️ Technical Implementation

### Requirements
```bash
tensorflow>=2.8.0
scikit-learn>=1.0.0
pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.5.0
scipy>=1.7.0
