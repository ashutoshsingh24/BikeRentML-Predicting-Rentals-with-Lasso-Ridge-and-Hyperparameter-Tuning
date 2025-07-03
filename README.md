# 🚲 Bike Sharing Demand Prediction

This project builds a regression model to predict daily bike rental counts using L1 (Lasso) and L2 (Ridge) regularization techniques with hyperparameter tuning via GridSearchCV and RandomizedSearchCV.

---

## 📂 Dataset

- **Name:** Bike Sharing Dataset
- **File:** `bike_sharing_daily.csv`
- **Source:** UCI Machine Learning Repository
- **Target Variable:** `cnt` (total bike rentals per day)

---

## 🧠 Objective

Predict the number of daily bike rentals using weather conditions and calendar features. 
Evaluate and compare models using Ridge and Lasso regression with different tuning techniques.

---

## 🛠️ Technologies Used

- Python 3
- Jupyter Notebook
- pandas, numpy
- scikit-learn (Ridge, Lasso, GridSearchCV, etc.)

---

## 📊 Model Workflow

1. **Data Cleaning**  
   Dropped unnecessary columns like `instant`, `dteday`, `casual`, and `registered`.

2. **Feature Scaling**  
   Used `StandardScaler` to normalize numerical features.

3. **Train-Test Split**  
   80% training / 20% testing.

4. **Modeling**  
   - Ridge Regression (L2 Regularization)
   - Lasso Regression (L1 Regularization)

5. **Hyperparameter Tuning**  
   - Grid Search (`GridSearchCV`)
   - Randomized Search (`RandomizedSearchCV`)

6. **Evaluation Metrics**  
   - Root Mean Squared Error (RMSE)
   - R² Score
   - Custom accuracy within tolerance

---

## 🧪 Results

| Model                | RMSE    |
|---------------------|---------|
| Ridge (Grid Search) | 832.84  |
| Ridge (Random Search)| 832.89 |
| Lasso (Grid Search) | ✅ **832.79** |
| Lasso (Random Search)| 832.79 |

- **Best Model:** Lasso with Grid Search
- **Custom Accuracy (±500):** ~73–78% (based on tolerance)
- **R² Score:** ~0.85–0.88 (explains most variance)

---

## 📈 Conclusion

- Lasso (L1) regression slightly outperformed Ridge (L2) regression.
- Hyperparameter tuning significantly improved model generalization.
- RMSE of ~833 indicates good performance relative to rental counts.

---

## 🔮 Future Improvements

- Try advanced models: Random Forest, XGBoost, or Gradient Boosting
- Feature engineering: add weekend/holiday flags, lag features
- Time-series or ensemble modeling

---

## 📁 File Structure

📦 project/
┣ 📄 bike_sharing_daily.csv
┣ 📘 bike_regression_project.ipynb
┗ 📘 README.md
