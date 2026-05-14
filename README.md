# ⚡ Smart Grid Electricity Demand Forecasting
**AI-driven Load Prediction using XGBoost & Time-Series Features**

AI-based electricity demand forecasting system for smart grids using machine learning and contextual time-series features.

---

## 📌 Problem Statement
Electricity demand changes dynamically due to weather conditions, industrial activity, human behavior, and holidays. Incorrect forecasting can lead to power wastage, grid overload, and inefficient distribution. This project predicts next-day hourly demand to support smarter load scheduling and grid optimization.

## 🚀 Features
* ✅ **Hourly Forecasting:** High-resolution demand prediction.
* ✅ **Weather-Integrated:** incorporates temperature and atmospheric data.
* ✅ **XGBoost Engine:** Robust nonlinear pattern recognition for structured data.
* ✅ **Interactive Dashboard:** Built with **Gradio** for real-time tracking.
* ✅ **Dynamic Visualization:** Plotly graphs for trend and peak demand analysis.
* ✅ **Smart-Grid Ready:** Comprehensive deployment strategy for infrastructure integration.

## 🛠️ Technologies Used
* **Language:** Python
* **Data Science:** Pandas, NumPy, Scikit-learn
* **Machine Learning:** XGBoost
* **Visualization:** Plotly, Matplotlib
* **Deployment/UI:** Gradio, Joblib

---

## ⚙️ Machine Learning Workflow


[Image of machine learning workflow diagram]

1. **Dataset Collection:** Integration of Energy & Weather historical data.
2. **Preprocessing:** Data cleaning and handling of missing values.
3. **Feature Engineering:** Time encoding (Sin/Cos), lag features, and holiday detection.
4. **XGBoost Training:** Model optimization for regression tasks.
5. **Forecast Generation:** Generating future load waveforms.
6. **Visualization & Evaluation:** KPI tracking and dashboard deployment.

## 📊 Features Used for Forecasting
| Feature | Description |
| :--- | :--- |
| **Hour** | Hour of the day (Cyclical Sin/Cos Encoding) |
| **Day of Week** | Weekday vs. Weekend information |
| **Month** | Seasonal effect tracking |
| **Lag Features** | Previous Hour and Previous Day load patterns |
| **Temperature** | Impact of weather on consumption |
| **Holiday Encoding** | Specialized behavior for non-working days |

## 📈 Model Performance & Results
Utilizing the **XGBoost Regressor** (Extreme Gradient Boosting), the model achieves high accuracy:

| Metric | Value |
| :--- | :--- |
| **RMSE (Root Mean Squared Error)** | **~588 MW** |
| **MAPE (Mean Absolute Percentage Error)** | **~1.37%** |

$$RMSE = \sqrt{\frac{1}{n}\sum_{i=1}^{n}(y_i - \hat{y}_i)^2}$$

---

## 📂 Project Structure
```text
electricity-demand-forecaster/
│
├── energy_dataset.csv     # Historical hourly electricity demand
├── weather_features.csv    # Temperature & atmospheric information
├── model.pkl              # Trained XGBoost model (Serialized)
├── train_model.py         # Data processing & model training script
├── app.py                 # Gradio Dashboard & UI logic
└── README.md              # Project Documentation

▶️ Installation & Execution
Install Dependencies:
pip install pandas numpy matplotlib scikit-learn xgboost gradio plotly joblib

Train the Model:
python train_model.py

Launch Dashboard:
python app.py

🌍 Real-World Applications
Designed for integration with:

Smart Meters: Real-time feedback for local load management.

Electricity Markets (IEX): Correlation of demand with pricing.

Grid Infrastructure: Deployment ready for entities like MESCOM.

👨‍💻 Developed By
Team: Fusion Techathon Project

Domain: Energy / Infrastructure

Core Architect: Hitesh Rajpurohit

📌 Conclusion
This project demonstrates how machine learning and the XGBoost algorithm can support more efficient energy management through accurate, contextual electricity demand forecasting.
