# Vehicle Maintenance Prediction using Neural Networks

This project demonstrates the application of **Artificial Neural Networks (ANNs)** for predictive maintenance in vehicles. The goal is to analyze vehicle data and predict whether maintenance is required, based on various characteristics such as mileage, battery status, and brake condition.

---

## 📋 Project Overview

Predictive maintenance is a critical strategy for reducing costs, improving vehicle reliability, and minimizing unexpected failures. This project uses a dataset of vehicle characteristics and maintenance history to train a neural network model for binary classification:  
- **1**: Maintenance is required.  
- **0**: Maintenance is not required.

Key highlights of the project:  
- Data preprocessing: Cleaning, transforming, and selecting key features.  
- Neural network implementation using TensorFlow/Keras.  
- Model evaluation and visualization of results.  

---

## 🗂️ Dataset

The dataset was obtained from [Kaggle](https://www.kaggle.com/datasets/chavindudulaj/vehicle-maintenance-data). It contains the following attributes:  

- **Vehicle characteristics:**  
  - `Vehicle_Model`, `Fuel_Type`, `Transmission_Type`, `Vehicle_Age`.  
- **Performance metrics:**  
  - `Mileage`, `Brake_Condition`, `Battery_Status`.  
- **Maintenance history:**  
  - `Last_Service_Date`, `Maintenance_History`, `Reported_Issues`.  
- **Target variable:**  
  - `Need_Maintenance` (1 for "Yes", 0 for "No").  

---

## 🛠️ Technologies Used

- **Programming Language:** Python  
- **Libraries and Frameworks:**  
  - `pandas`, `numpy`: Data manipulation.  
  - `matplotlib`, `seaborn`: Data visualization.  
  - `TensorFlow/Keras`: Neural network implementation.  
  - `scikit-learn`: Data preprocessing and splitting.  

---

## 📊 Project Workflow

### **1. Data Preprocessing**
- Removed duplicates and handled missing values.  
- Converted categorical columns into numerical values using *one-hot encoding*.  
- Transformed date columns (`Last_Service_Date`, `Warranty_Expiry_Date`) into numerical features (e.g., days since last service).  
- Visualized correlations between features using a heatmap.  

### **2. Neural Network Implementation**
The neural network was designed with the following architecture:  
- **Input Layer:** 20 features.  
- **Hidden Layers:**  
  - Layer 1: 64 neurons, ReLU activation.  
  - Layer 2: 32 neurons, ReLU activation.  
- **Output Layer:** 1 neuron, Sigmoid activation (binary classification).  

### **3. Training and Evaluation**
- Training:  
  - Optimizer: Adam.  
  - Loss function: Binary crossentropy.  
  - Batch size: 32, Epochs: 100.  
- Model achieved ~100% accuracy on test data.  
- Visualized performance with loss and accuracy plots.  

---

## 📈 Results

- **Model Performance:**  
  - High accuracy (~100%) on test data.  
  - Key features influencing predictions: `Reported_Issues`, `Worn_Out_Brake`, `Weak_Battery`.  

- **Sample Prediction:**  
  For a single vehicle:  
  - **Predicted Value:** 1 (Maintenance required).  
  - **Actual Value:** 1.  

---

## 📌 Key Learnings and Limitations

### **Key Learnings**
- Neural networks are effective for analyzing vehicle data and predicting maintenance needs.  
- Preprocessing steps like one-hot encoding and feature selection are crucial for model performance.  

### **Limitations**
- Imbalanced data: The dataset contains more samples where maintenance is not required.  
- Generalization: The model needs testing on other datasets to validate its robustness.  

---

## 🚀 Future Work

1. Use more advanced architectures, like Recurrent Neural Networks (RNNs), to analyze time-series data.  
2. Integrate real sensor data from vehicles (e.g., vibration, temperature) for better predictions.  
3. Deploy the model into a real-time monitoring system for vehicles.  

---

## 📬 Contact

For any questions or suggestions, feel free to reach out:
- **Author:** Darko Gligorijević
- **Email:** darkogligorijeviccc@gmail.com

---
