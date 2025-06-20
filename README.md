# Health Insurance Premium Predictor

An intelligent web application built with Streamlit that estimates individual health insurance premiums based on demographic, lifestyle, and medical inputs. By using separate regression models for different age segments, it delivers more tailored and accurate predictions.

## 🛠 Features  
- Interactive and clean Streamlit interface  
- Predicts premium cost based on user inputs like age, BMI, smoking status, income, etc.  
- Dual-model approach for better accuracy:
    - Linear Regression for younger users
    - XGBoost for the rest of the population
- Uses pre-trained and serialized models & scalers for real-time predictions  
- Lightweight, fast, and easy to run locally
- No database or backend server required

## 🚀 How to Run Locally  
### Prerequisites:  
- Python 3.8+

1. **Clone the repository**:
   ```bash
   git clone https://github.com/vaibhavgarg2004/Health Insurance Premium Predictor.git
   cd Health Insurance Premium Predictor
   ```
2. **Install dependencies**:   
   ```commandline
    pip install -r requirements.txt
   ```
5. **Run the Streamlit app**:   
   ```commandline
    streamlit run main.py
   ```

## 📂 Project Structure

```
Health_Insurance_Cost_Predictor/
│
├── artifacts/                      # Serialized models and scalers
│   ├── model_rest.joblib           # XGBoost model for the general adult population
│   ├── model_young.joblib          # Linear Regression model for younger users
│   ├── scaler_rest.joblib          # StandardScaler fitted on “rest” training data
│   └── scaler_young.joblib         # StandardScaler fitted on “young” training data
│
├── LICENSE                         # Apache License file
├── README.md                       # This documentation
├── main.py                         # Streamlit app logic
├── prediction_helper.py            # Model loading and prediction logic
└── requirements.txt                # Python dependencies
```

## 🖼️ Application Snapshot

![Application UI](insurance_predictor_ui_mockup.png)

---
Built with ❤️ using Streamlit, Scikit-learn, and XGBoost

