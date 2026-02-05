# 🚖 Ride-Flow: Dynamic Pricing & Decision-Making Engine

### 📊 Project Overview
This project develops a data-driven pricing engine for a ride-sharing service. By analyzing supply-demand dynamics, the model optimizes fares in real-time, ensuring a balance between driver availability and customer demand.

### 🧠 The Business Problem
Ride-sharing platforms face a "Supply-Demand Mismatch." During peak hours, demand is high but supply is low. This project solves this by:
1. **Predicting Base Price** based on duration and historical data.
2. **Automating Surge Pricing** to incentivize drivers during high-demand periods.

### 🛠️ Strategic Feature Engineering
I engineered 4 key features that serve as the "brain" of the pricing logic:
- **Demand_Supply_Ratio**: The core signal for market pressure.
- **Supply_Gap**: Absolute shortage of drivers (Riders - Drivers).
- **Rider_Engagement**: Interaction between customer loyalty and ratings.
- **Cost_Per_Minute**: Efficiency metric of historical pricing.

### 🏆 Model Selection & Performance
I evaluated multiple models using **5-Fold Cross Validation**:
- **Linear Regression (Winner): 0.8732 R² Score**
- Random Forest: 0.8557 R² Score
- XGBoost: 0.8396 R² Score

*Insight: Linear Regression performed best, indicating a strong linear relationship between demand intensity and ride cost.*

### 🚀 Real-Time Inference & Decision Logic
The system implements a multi-tier surge strategy:
- **Extreme Demand (Ratio > 5.0)**: `+30% Surge Price`
- **High Demand (Ratio > 3.0)**: `+25% Surge Price`
- **Low Demand (Ratio < 0.8)**: `-20% Discount` to boost bookings.

### 📂 Repository Structure
- `Notebook.ipynb`: End-to-end ML pipeline (EDA, Training, Validation).
- `rides_data.csv`: 1,000+ rows of ride-sharing market data.
- `final_model.pkl`: Serialized Linear Regression model for deployment.
- `scaler.pkl`: Pre-fitted StandardScaler for real-time inference.

### 💻 Tech Stack
- **Language:** ![Python](https://img.shields.io)
- **Libraries:** ![Pandas](https://img.shields.io) ![Scikit-Learn](https://img.shields.io) ![NumPy](https://img.shields.io)
- **Visualization:** ![Matplotlib](https://img.shields.io) ![Seaborn](https://img.shields.io)

---
*Developed as a Strategic Decision-Making Project for Ride-Sharing Analytics.*


