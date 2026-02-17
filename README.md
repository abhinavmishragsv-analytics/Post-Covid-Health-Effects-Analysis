NeuroRisk AI – Post-COVID Brain Fog Screening Tool

An explainable machine learning-based clinical decision support prototype designed to assist in early screening of post-COVID cognitive impairment risk.

📌 Problem Statement

Post-COVID patients often report cognitive symptoms such as “brain fog,” fatigue, and mental health disturbances. However, early identification of high-risk individuals remains challenging in clinical settings.

NeuroRisk AI is a lightweight, interpretable ML prototype that estimates the probability of brain fog occurrence using structured health data.

This tool is designed for:

Early screening

Risk stratification

Clinical monitoring support

⚠️ This is a screening support tool, not a diagnostic system.

📊 Dataset

Size: 500 × 12

Target: Brain Fog (Yes/No)

Features:

Demographics

COVID severity

Fatigue level

Mental health impact

Physical activity level

Recovery duration

Long COVID indicators

Class distribution:

25% Brain Fog (Yes)

75% Brain Fog (No)

🧠 Model Architecture

Model Used: Logistic Regression
Why Logistic Regression?

Interpretable

Clinically explainable

Suitable for small tabular datasets

Transparent coefficient analysis

Preprocessing:

One-hot encoding for categorical features

Standard scaling for numeric features

Class-weight balancing

5-fold cross-validation

Threshold optimization for recall prioritization

📈 Model Performance

Cross-validated ROC-AUC ≈ 0.60

Recall optimized for screening sensitivity

Probability range: 0.16 – 0.89

This performance reflects moderate predictive separation typical of small clinical datasets.

🔎 Explainability (SHAP Integration)

Global feature drivers identified:

Fatigue Level

Mental Health Impact

COVID Severity

Days to Recovery

Physical Activity Level

Local patient-level explanations provided via SHAP force plots.

This ensures:

Transparency

Trust

Clinical interpretability

🏥 Product Features

✔ Risk Score (0–100%)
✔ Risk Category (Low / Moderate / High)
✔ Colored risk visualization
✔ Clinical recommendation logic
✔ Interactive notebook-based UI (Colab)
✔ SHAP feature attribution panel

💡 Example Output

Risk Score: 58.4%
Risk Category: MODERATE

Key Contributors:

Elevated fatigue level

Moderate COVID severity

Extended recovery duration

Recommended Action:
Monitor cognitive symptoms over the next 2–4 weeks.

🏗 System Flow

Raw Data
→ Preprocessing
→ Logistic Regression
→ Probability Scoring
→ SHAP Explainability
→ Risk Dashboard Output

⚠️ Limitations

Dataset limited to 500 samples

No longitudinal clinical markers

No lab/imaging data

Not externally validated

Intended for educational and prototype purposes only

🚀 Future Improvements

Larger clinical dataset

Longitudinal modeling

XGBoost/CatBoost comparison

API deployment (FastAPI)

Streamlit cloud deployment

PDF risk report export
