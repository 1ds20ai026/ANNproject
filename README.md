# ChurnGuard AI

Customer Churn Prediction System
Project Overview
This project implements a machine learning system to predict customer churn in a banking context. It uses artificial neural networks (ANN) to analyze customer data and predict the likelihood of a customer leaving the bank's services.
Technical Architecture
1. Data Processing Pipeline

Input Data Processing

Removes irrelevant columns (RowNumber, CustomerId, Surname)
Handles categorical variables:

Gender: Label encoded (Male/Female → 0/1)
Geography: One-hot encoded (Countries → Binary columns)


Scales numerical features using StandardScaler



2. Machine Learning Model

Neural Network Architecture

Input Layer: Matches preprocessed feature dimensions
Hidden Layer 1: 64 neurons with ReLU activation
Hidden Layer 2: 32 neurons with ReLU activation
Output Layer: 1 neuron with Sigmoid activation (for binary classification)



3. Model Training

Uses binary crossentropy loss function
Adam optimizer with 0.01 learning rate
Implements early stopping to prevent overfitting
Includes TensorBoard integration for monitoring

4. Deployment

Streamlit web interface for real-time predictions
Saves and loads:

Trained model (.h5 format)
Label encoders (pickle files)
One-hot encoders (pickle files)
Feature scaler (pickle files)



Features Analyzed

Credit Score
Geography (France, Spain, Germany)
Gender
Age
Tenure
Balance
Number of Products
Has Credit Card
Is Active Member
Estimated Salary

User Interface
The Streamlit app provides:

Input fields for all customer features
Real-time prediction of churn probability
Clear indication of whether a customer is likely to churn
Interactive sliders and dropdown menus for easy data input

Potential Business Applications

Proactive Customer Retention
Risk Assessment
Customer Service Prioritization
Marketing Campaign Targeting
Product Development Insights
