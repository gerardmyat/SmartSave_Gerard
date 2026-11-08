# 💰 Smart Savings

ICT336 workshop: A savings website powered by 2 Machine Learning models built on Kaggle datasets.

- **Tab 1: Fixed Deposit**: Supervised classification model that predicts if a bank customer is likely to open a fixed deposit account.
- **Tab 2: Saver Group**: Unsupervised K-Means clustering model that categorizes customers into financial behavioral personas based on annual income and spending score.
- **Tab 3: About the Models**: Details on model architectures, metrics (F1 score, confusion matrix), and datasets.

---

## 🚀 Getting Started

### Prerequisites
- Python 3.10+ (Python 3.12 recommended)
- [`uv`](https://docs.astral.sh/uv/) (optional, recommended) or standard `pip`

### 1. Setup Virtual Environment

Using `uv`:
```bash
uv venv --python 3.12
.venv\Scripts\activate
uv pip install -r requirements.txt
```

Or using standard Python:
```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```

### 2. Run the Streamlit App

With the virtual environment activated:
```bash
streamlit run app.py
```

Alternatively:
```bash
.\.venv\Scripts\streamlit run app.py
```

The app will start at `http://localhost:8501`.

---

## 🌐 GitHub Pages (In-Browser Execution)

`index.html` uses [stlite](https://github.com/whitphx/stlite) (Streamlit compiled to WebAssembly via Pyodide) to run the Python application entirely client-side in the browser without needing a Python backend server.

To host on GitHub Pages:
1. Go to repository **Settings** -> **Pages**.
2. Select **Source** as `Deploy from a branch` -> `main` / `root`.
3. Save, and your app will be live at `https://gerardmyat.github.io/SmartSave_Gerard/`.

---

## 📁 Project Structure

- `app.py`: Main Streamlit web application.
- `savings_model.joblib`: Pretrained supervised classification model pipeline for fixed deposit prediction.
- `saver_model.joblib`: Pretrained K-Means clustering model for customer segmentation.
- `customers_with_groups.csv`: Mall customer segmentation dataset with group assignments.
- `index.html`: Client-side stlite wrapper for GitHub Pages deployment.
- `requirements.txt`: Python dependencies (`streamlit`, `pandas`, `scikit-learn>=1.7.2`, `joblib`).
- `.streamlit/config.toml`: Streamlit configuration settings.
