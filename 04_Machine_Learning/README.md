# Phase 4 — Machine Learning

Machine learning enables systems to learn patterns from data and make predictions or decisions without being explicitly programmed. This phase covers classical ML — the algorithms that still power most production systems today.

---

## Learning Steps

### 1. Supervised Learning
- **Regression:** Linear Regression, Ridge, Lasso, Elastic Net
- **Classification:** Logistic Regression, Decision Trees, Random Forest, SVM, k-NN
- **Ensemble Methods:** Gradient Boosting, XGBoost, LightGBM, AdaBoost
- Feature engineering, selection, and importance

### 2. Unsupervised Learning
- **Clustering:** k-Means, DBSCAN, Hierarchical Clustering
- **Dimensionality Reduction:** PCA, t-SNE, UMAP
- **Anomaly Detection:** Isolation Forest, LOF

### 3. Model Evaluation
- Train / validation / test split, cross-validation (k-fold, stratified k-fold)
- Classification metrics: Accuracy, Precision, Recall, F1, ROC-AUC, Confusion Matrix
- Regression metrics: MAE, RMSE, R²
- Bias-variance tradeoff, overfitting vs underfitting, regularization (L1/L2)

### 4. Pipelines & Production
- Scikit-learn Pipelines: preprocessing + model in one object
- Hyperparameter tuning: GridSearchCV, RandomizedSearchCV, Optuna
- Model serialization: joblib, pickle
- MLflow for experiment tracking and model registry

---

## Tools & Libraries

| Tool | Purpose |
|------|---------|
| **Scikit-learn** | The standard ML library — regression, classification, clustering, evaluation metrics, pipelines |
| **XGBoost** | Gradient boosting for tabular prediction — demand forecasting, business ML, competitions |
| **LightGBM** | Fast gradient boosting for large datasets |
| **Pandas + NumPy** | Feature engineering and data preparation |
| **MLflow** | Experiment tracking, model registry, deployment |
| **DVC** | Data version control alongside Git |
| **Weights & Biases** | Experiment visualization and hyperparameter sweeps |
| **Optuna** | Hyperparameter optimization framework |

---

## PDF Resources

* [Pandas Cheat Sheet](./Pandas_Cheat_Sheet.pdf)
* [Machine Learning Cheat Sheet](./ML+Cheat+Sheet_2.pdf)
* [Scikit-Learn Cheat Sheet](./Scikit-Learn_Cheat_Sheet.pdf)
* [Supervised Machine Learning Models](./Supervised_Machine_Learning_Models.pdf)
* [Unsupervised Machine Learning Models](./Unsupervised_Machine_Learning_Models.pdf)

---

## Learning Resources

- [Kaggle: Intro to Machine Learning](https://www.kaggle.com/learn/intro-to-machine-learning)
- [Kaggle: Intermediate Machine Learning](https://www.kaggle.com/learn/intermediate-machine-learning)
- [ML RoadMap Bangla](https://www.youtube.com/playlist?list=PLKdU0fuY4OFfWY36nDJDlI26jXwInSm8f)
- [Scikit-learn User Guide](https://scikit-learn.org/stable/user_guide.html)
- [XGBoost Documentation](https://xgboost.readthedocs.io/)
- [Hands-On ML with Scikit-Learn, Keras & TensorFlow — Aurélien Géron](https://github.com/ageron/handson-ml3)
- [ML Lifecycle from Data Ingestion to Model Deployment (Snowflake)](https://www.snowflake.com/en/developers/guides/first-machine-learning-project/)
