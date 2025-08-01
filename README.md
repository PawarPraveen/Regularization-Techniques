#  Regularization Techniques in Machine Learning

This repository explains the most widely-used regularization techniques for regression problems:

-  Lasso Regression
-  Ridge Regression
-  ElasticNet
-  Random Forest Regressor
-  XGBoost Regressor

---

##  Why Regularization?

Regularization is used to **prevent overfitting** by penalizing large model weights. This improves the model’s **generalization** ability on unseen data.

When you see your model perform **very well on training data** but **poorly on test data**, it's likely overfitting. Regularization helps fix that.

---

##  1. Lasso Regression (L1 Regularization)

###  How it works:
- Adds **L1 penalty**: `Loss + α * |coefficients|`
- Can **shrink some coefficients to zero** → performs **feature selection**

###  When to use:
- When you suspect **many features are irrelevant**
- When you want to **reduce model complexity**

###  Pros:
- Good for sparse feature selection
- Easy to interpret

###  Cons:
- Can underperform when many features are correlated

## 2. Ridge Regression (L2 Regularization)
 How it works:
Adds L2 penalty: Loss + α * sum(coefficients²)

Shrinks all coefficients but does not eliminate any

 When to use:
When all features are relevant and multicollinearity is present

 Pros:
Works well when features are highly correlated

Better numerical stability than Lasso

## 3. ElasticNet (L1 + L2 Regularization)
 How it works:
Combines L1 and L2 penalties

Uses a mixing parameter l1_ratio (0 = Ridge, 1 = Lasso)

 When to use:
When you want benefits of both Lasso and Ridge

Useful when some features are irrelevant and some are correlated

## 4. Random Forest Regressor (Ensemble Tree-Based)
 How it works:
Builds multiple decision trees and averages their results

Built-in feature selection and robust to outliers

 When to use:
When you need non-linear modeling and don't want to manually select features

 Pros:
No need for scaling

Handles missing values & nonlinearities well

## 5. XGBoost Regressor (Extreme Gradient Boosting)
 How it works:
Boosts weak learners sequentially

Uses regularization (L1 & L2) built-in

 When to use:
When you want state-of-the-art accuracy

Best choice for structured/tabular data

 Pros:
Fast and accurate

Built-in handling for regularization and missing values


| Method        | Penalty            | Feature Selection | Use Case                                  |
| ------------- | ------------------ | ----------------- | ----------------------------------------- |
| Lasso         | L1                 |  Yes             | Sparse models with few important features |
| Ridge         | L2                 |  No              | Multicollinear data, all features useful  |
| ElasticNet    | L1 + L2            |  Partial         | Mixed scenario                            |
| Random Forest | None               |  Implicit        | Non-linear, robust models                 |
| XGBoost       | L1 + L2 (Built-in) |  Smart selection | High-performance models with tuning       |

