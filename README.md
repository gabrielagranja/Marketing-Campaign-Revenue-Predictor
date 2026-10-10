# 📈 Marketing Campaign Revenue Predictor

A **Machine Learning** project built during the Artificial Intelligence Bootcamp. It predicts the expected revenue of digital marketing campaigns using regression techniques.

The solution covers the full lifecycle of an ML project: dataset analysis, EDA, model training, tuning, deployment with Streamlit and containerization with Docker.

**🌐 Demo:** https://ai-project-regression-marketing-nfcaunp8mbcgqybcz3wr74.streamlit.app/

> The demo runs on Streamlit Community Cloud's free tier, so it may take a few seconds to wake up after a period of inactivity.

---

# 🎯 Goal

Build a model that estimates a campaign's **Revenue** from its performance and planning metrics (such as clicks, conversions, spend and campaign objective).

The project started as a **Linear Regression** exercise. After comparing several regression algorithms, an **optimized Random Forest Regressor** was selected because it delivered better predictive performance.

---

# 🛠 Tech stack

* Python
* Pandas
* NumPy
* Scikit-Learn
* RandomizedSearchCV
* Matplotlib
* Streamlit
* Joblib
* Docker
* Git & GitHub

---

# 📂 Project structure

```text
.
├── app/
│   └── streamlit_app.py
├── data/
│   ├── digital_marketing_dataset_30k.csv
│   ├── data_dictionary.csv
│   └── README_DATASET.md
├── docs/
├── models/
│   └── campaign_revenue_forecast_model.joblib
├── notebooks/
├── src/
├── tests/
├── Dockerfile
├── requirements.txt
└── README.md
```

---

# 🤖 Model

The end-to-end workflow includes:

* Data cleaning and preparation.
* Missing value imputation.
* Scaling of numerical features.
* One-hot encoding of categorical features.
* Scikit-Learn Pipeline.
* Training of several regression models.
* Hyperparameter tuning with **RandomizedSearchCV**.
* Export of the trained model with Joblib.

Final model:

**Optimized Random Forest Regressor**

---

# 📊 Results

## Evaluation metrics (test set)

| Metric | Value      |
| ------ | ---------: |
| MAE    |     177.58 |
| MSE    | 1.35 × 10⁶ |
| RMSE   |    1160.78 |
| R²     |      0.850 |

The model explains about **85% of the variance in Revenue**.

---

## 📉 Overfitting check

| Metric          |   Value |
| --------------- | ------: |
| Training R²     |  0.9688 |
| Testing R²      |  0.8483 |
| Overfitting gap |  0.1204 |
| Overfitting (%) | 12.04 % |

Training and test performance were compared throughout the project to monitor overfitting before choosing the final version.

---

## 🔍 Most important features

Feature importance analysis showed that the variables with the greatest influence on the predictions were:

1. Number of conversions
2. Number of clicks
3. Objective: Leads
4. Objective: Sales
5. Spend

The top ten features account for about **96% of the model's cumulative importance**.

---

# 🚀 Installation

Clone the repository:

```bash
git clone https://github.com/gabrielagranja/Marketing-Campaign-Revenue-Predictor.git
cd Marketing-Campaign-Revenue-Predictor
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate it:

### Windows

```bash
.venv\Scripts\activate
```

### Linux / macOS

```bash
source .venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

# 💾 Required files

The app needs:

```text
data/digital_marketing_dataset_30k.csv

models/campaign_revenue_forecast_model.joblib
```

---

# ▶️ Run the app

```bash
streamlit run app/streamlit_app.py
```

Open:

```
http://localhost:8501
```

---

# 🐳 Docker

Build the image:

```bash
docker build -t marketing-regression-app .
```

Run the container:

```bash
docker run -p 8501:8501 marketing-regression-app
```

---

# ☁️ Deployment

The project is deployed on **Streamlit Community Cloud**.

It also ships as a fully **containerized** version, ready to deploy on any Docker-compatible platform.

---

# 📌 Project status

Delivered version:

**MVP v0.1**

Includes:

* ✅ Documented dataset
* ✅ Exploratory Data Analysis (EDA)
* ✅ Feature engineering
* ✅ Regression modeling
* ✅ Model comparison
* ✅ Model tuning
* ✅ Metric-based evaluation
* ✅ Streamlit app
* ✅ Dockerization
* ✅ Deployment
* ✅ Documentation

---

# 🔮 Next steps

* Prediction history.
* Database.
* Interactive dashboard.
* Report export.
* Model monitoring.
* Automatic retraining.
* Authentication.

---

# 👩‍💻 Author

**Gabriela Granja**

Artificial Intelligence Bootcamp

2026
