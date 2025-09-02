# Distributor Loyalty Score Bot (Churn Prediction with XGBoost)

> Predict distributor/customer churn using an XGBoost-based pipeline with class-imbalance handling, model explainability (SHAP), and an optional Streamlit app for interactive scoring.

![Banner](docs/cover.png)

## 🚀 Features
- End-to-end churn workflow: data prep → imbalance handling (SMOTE) → XGBoost training → evaluation (ROC AUC, F2-score) → SHAP insights.
- Reproducible environment with `requirements.txt`.
- Clean repository layout and GitHub Actions CI.
- Notebook-first development (`notebooks/`), with a path to production code (`src/`).

## 📦 Project Structure
```
distributor-loyalty-score-bot/
├─ notebooks/
│  └─ Distributor-loyalty-score-bot.ipynb
├─ data/
│  ├─ README.md
│  └─ sample_distributor_dataset.csv   # small sample for demo
├─ src/
│  ├─ __init__.py
│  ├─ train.py                         # (optional) move notebook logic here
│  ├─ inference.py                     # (optional) batch/real-time scoring
│  └─ app.py                           # (optional) Streamlit UI
├─ models/                             # (ignored) trained artifacts
├─ docs/
│  └─ cover.png                        # add a banner (optional)
├─ .github/workflows/ci.yml            # lint/build checks
├─ .gitignore
├─ LICENSE
├─ requirements.txt
└─ README.md
```

## 🗂️ Data
- Keep **raw data private**. Place only **small, anonymized samples** in `data/`.- `data/sample_distributor_dataset.csv` shows the expected schema (first few hundred rows).- Add your full dataset locally but **do not commit** it (see `.gitignore`).

## 🧪 Quickstart
```bash
# 1) Create & activate a virtual environment (conda or venv)
python -m venv .venv && source .venv/bin/activate  # on Windows: .venv\Scripts\activate

# 2) Install deps
pip install -r requirements.txt

# 3) Explore the notebook
jupyter notebook notebooks/Distributor-loyalty-score-bot.ipynb

# 4) (Optional) Train via script
python src/train.py

# 5) (Optional) Run Streamlit app
streamlit run src/app.py
```

## 📈 Evaluation
- Primary metrics: **ROC AUC**, **F2-score** (recall-focused), plus confusion matrix, precision/recall.- Use **SHAP** to interpret top churn drivers and guide retention actions.

## 🛠️ Tech
- Python, Pandas, NumPy, scikit-learn, **XGBoost**, imbalanced-learn (SMOTE), SHAP, Matplotlib/Seaborn.- (Optional) Streamlit for UI.

## 🤝 Contributing
See [CONTRIBUTING.md](CONTRIBUTING.md).

## 📄 License
This project is licensed under the **MIT License**. See [LICENSE](LICENSE).

---

> Tip: Add repo **Topics** (e.g., `churn-prediction`, `xgboost`, `customer-analytics`), pin the repo, and include a short description for better discoverability.
