# Network Intrusion Detection and Response System

## Overview
This project is a Network Intrusion Detection and Response System that leverages machine learning to classify network packets as normal or anomalous (potential attacks). It provides:
- An interactive Streamlit web app for packet classification
- Data science workflow in a Jupyter notebook for model training and evaluation
- Quantum circuit simulation tools for research and experimentation
- Pre-trained ML model and sample datasets

## Features
- **Interactive Web App:** Enter packet features and get real-time predictions (normal/anomalous)
- **ML Model:** Trained on simulated network traffic and attack data
- **Quantum Tools:** Scripts for parsing and simulating quantum circuits
- **Data Science Workflow:** Full pipeline from data loading, preprocessing, feature selection, model training (Decision Tree, SVM, KNN, Naive Bayes, DQN), to evaluation

## Dependencies
Install the following Python packages:
- streamlit
- scikit-learn
- numpy
- pandas
- matplotlib
- joblib
- scapy (for packet sniffing, in the notebook)
- tensorflow, keras (for DQN in the notebook)
- qiskit, qiskit-aer (for quantum circuit simulation)

You can install the main dependencies with:
```bash
pip install streamlit scikit-learn numpy pandas matplotlib joblib qiskit qiskit-aer tensorflow scapy
```

## Usage

### 1. Web App
Run the Streamlit app for packet classification:
```bash
streamlit run app.py
```
- Enter packet parameters in the UI
- Click "Predict" to see if the packet is normal or anomalous

### 2. Model Training & Data Analysis
Open `IDS_1.ipynb` in Jupyter Notebook to:
- Explore the dataset
- Train and evaluate models
- Experiment with feature engineering and RL-based response

### 3. Quantum Circuit Simulation
- `q.py` runs a simple socket server to simulate quantum circuits described in a custom text format
- `trial.py` parses and prints quantum gate instructions

## Data
- `Train_data.csv` and `Test_data.csv` are used for model training and evaluation
- Features are based on the KDD Cup 99 dataset (simulated military network traffic with labeled attacks)

## File Descriptions
- `app.py`: Streamlit web app for packet classification
- `IDS_1.ipynb`: Main notebook for data science workflow
- `ids_model1.joblib`: Pre-trained ML model
- `q.py`: Quantum circuit simulation server
- `trial.py`: Quantum instruction parser
- `Train_data.csv`, `Test_data.csv`: Datasets

## Example
1. Start the app:
   ```
   streamlit run app.py
   ```
2. Enter features (e.g., protocol: tcp, service: http, src_bytes: 100, etc.)
3. Click "Predict" to classify the packet

## Notes
- For real-time packet sniffing and advanced RL-based response, see the notebook
- Quantum scripts are experimental and require Qiskit
