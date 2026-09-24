# 🏠 House Price Prediction

**IBM Internship Project**  
**Author:** Gaurav Singh Juneja  
**Dataset:** [California Housing Dataset](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.fetch_california_housing.html) (built into scikit-learn)

---

## 📌 Project Description

This project builds an end-to-end **Machine Learning pipeline** to predict median house prices based on socioeconomic and geographical features from the California Housing dataset. The project covers data exploration, feature engineering, model training, hyperparameter tuning, and deployment-ready model export.

### Key Highlights
- Compares **6 regression models**: Linear Regression, Ridge, Lasso, Decision Tree, Random Forest, Gradient Boosting
- Best model: **Tuned Random Forest** achieving **R² ≈ 0.83+**
- Full EDA with correlation heatmaps, distribution plots, and scatter plots
- Feature importance analysis
- Model and scaler serialized with `joblib` for deployment

---

## 📂 Repository Structure

```
ibm-internship/
├── GauravSinghJuneja_HousePricePrediction.ipynb  ← Complete ML notebook (Code File)
├── requirements.txt                               ← Python dependencies
├── README.md                                      ← This file
├── GauravSinghJuneja_ProjectReport.docx           ← Full project report
└── models/                                        ← Saved model & scaler (generated on run)
    ├── house_price_model.pkl
    └── scaler.pkl
```

---

## 🛠️ Technologies Used

| Category | Libraries / Tools |
|---|---|
| Language | Python 3.10+ |
| ML Framework | scikit-learn |
| Data Handling | pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Web Backend | Flask, Flask-CORS |
| Web Frontend | Streamlit |
| Notebook | Jupyter Notebook |
| Model Persistence | joblib |

---

## 📊 Dataset

**California Housing Dataset** — built into `scikit-learn`

| Feature | Description |
|---|---|
| MedInc | Median income in block group |
| HouseAge | Median house age in block group |
| AveRooms | Average number of rooms per household |
| AveBedrms | Average number of bedrooms per household |
| Population | Block group population |
| AveOccup | Average number of household members |
| Latitude | Block group latitude |
| Longitude | Block group longitude |
| **MedHouseVal** | **Target — Median house value (in $100,000s)** |

- **Samples:** 20,640  
- **Features:** 8 (+ 3 engineered)  
- **No missing values**

---

## 🚀 Setup & Run Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/gsjuneja226/ibm-internship.git
cd ibm-internship
```

### 2. Create a Virtual Environment (Recommended)
```bash
python -m venv venv
# Windows
venv\Scripts\activate
# macOS/Linux
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Run the Jupyter Notebook
```bash
jupyter notebook GauravSinghJuneja_HousePricePrediction.ipynb
```
Run all cells sequentially (Cell → Run All).

---

## 📈 Model Results

| Model | MAE | RMSE | R² Score |
|---|---|---|---|
| Linear Regression | ~0.53 | ~0.73 | ~0.60 |
| Ridge Regression | ~0.53 | ~0.73 | ~0.60 |
| Lasso Regression | ~0.53 | ~0.73 | ~0.60 |
| Decision Tree | ~0.45 | ~0.63 | ~0.70 |
| Random Forest | ~0.35 | ~0.51 | ~0.80 |
| **Tuned Random Forest** | **~0.33** | **~0.48** | **~0.83** |

> Exact values are printed when the notebook is executed.

---

## 🔑 Key Findings

1. **MedInc (Median Income)** is by far the strongest predictor of house prices
2. **Geographical features** (Latitude, Longitude) are highly important
3. **Random Forest** significantly outperforms linear models on this dataset
4. Hyperparameter tuning further improved R² by ~2–3%
5. Engineered features (RoomsPerHousehold, BedroomsPerRoom) contributed marginally

---

## 📧 Contact

**Gaurav Singh Juneja**  
IBM Internship Program  
GitHub: [@gsjuneja226](https://github.com/gsjuneja226)
