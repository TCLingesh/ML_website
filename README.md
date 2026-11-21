# Multiple Disease Prediction System

A Streamlit web application for predicting **Diabetes**, **Heart Disease**, and **Parkinson's Disease** using pre-trained machine learning models loaded via `pickle`[cite: 1].

## Features

- **Sidebar Navigation (`streamlit-option-menu`)**: Switch between three prediction modules:
  - **Diabities System** (`diabetes_model_deploy.sav`) — Uses a trained model and feature scaler across 8 clinical features (`Pregnancies`, `Glucose`, `BloodPressure`, `SkinThickness`, `Insulin`, `BMI`, `DiabetesPedigreeFunction`, `Age`)[cite: 1].
  - **Heart Disease Prediction** (`heart_model.sav`) — Uses a trained model across 13 clinical and cardiac attributes (`age`, `sex`, `cp`, `trestbps`, `chol`, `fbs`, `restecg`, `thalach`, `exang`, `oldpeak`, `slope`, `ca`, `thal`)[cite: 1].
  - **Parkinsons Prediction** (`parkinsons_model.sav`) — Uses a trained model and feature scaler across 22 vocal/acoustic features (`MDVP:Fo(Hz)`, `MDVP:Fhi(Hz)`, `MDVP:Flo(Hz)`, jitter, shimmer, `NHR`, `HNR`, `RPDE`, `DFA`, `spread1`, `spread2`, `D2`, `PPE`)[cite: 1].

## Project Structure

```text
ML_website/
├── diabetes_model_deploy.sav   # Serialized diabetes model and scaler
├── heart_model.sav             # Serialized heart disease model
├── parkinsons_model.sav        # Serialized Parkinson's disease model and scaler
├── multiple_disease_predict.py # Main Streamlit application script
└── requirements.txt            # Python dependencies
```


## Installation & Usage

1. **Clone the repository**
   ```bash
   git clone [https://github.com/TCLingesh/ML_website.git](https://github.com/TCLingesh/ML_website.git)
   cd ML_website
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```
   *(Ensure `streamlit`, `streamlit-option-menu`, `numpy`, and `scikit-learn` are installed in the environment where the `.sav` files were created.)*

3. **Run the Streamlit app**
   ```bash
   streamlit run multiple_disease_predict.py
   ```

## Notes & Disclaimer

- All inputs in the current interface use `st.text_input`, so enter numeric values carefully and ensure all fields are populated before clicking a test result button[cite: 1].
- This application is for educational and demonstration purposes only and is **not** a substitute for professional medical diagnosis or advice.
