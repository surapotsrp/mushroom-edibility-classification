# 🍄 Predicting Mushroom Edibility with Machine Learning

This project predicts whether a mushroom is edible or poisonous based on physical characteristics. It compares Decision Tree and Random Forest models using cross-validation and statistical tests to determine the most reliable classification approach.

📄 **Full Report:** [Predict Edibility of Mushrooms (PDF)](./Predict%20edible%20of%20mushrooms.pdf)

---

## 📊 Project Overview

- **Goal:** Classify mushrooms as edible or poisonous (binary classification)
- **Input Features:** CapShape, CapSurface, CapColor, Odor, Height
- **Output Variable:** Edibility (0 = Edible, 1 = Poisonous)
- **Tools:** R (`rpart`, `randomForest`, `caret`, `dplyr`, `rpart.plot`)

---

## 🧪 Models Compared

### 🔸 Decision Tree  
- Tuned via `minsplit`, `cp`, `maxdepth` (grid search with 31 input combinations)  
- Best formula: `Edible ~ CapShape + CapSurface + CapColor + Odor`  
- **Best Accuracy:** 99.11%  
- Selected using 100x cross-validation  

### 🔸 Random Forest  
- Tuned via `ntree` (50–150), tested over same input combinations  
- Accuracy reached ~96%, but lower than Decision Tree  
- Slower computation, more sensitive to parameter tuning

---

## 🧠 Statistical Comparison

- Used 100-fold cross-validation for both models  
- **Paired t-test:** p-value ≈ 1.63e-13  
- 📌 **Conclusion:** Decision Tree outperforms Random Forest statistically in this task

---

## 📈 Visualisations

- Decision Tree visualised via `rpart.plot`
- Accuracy plots for parameter tuning  
- Histogram of model wins from cross-validation

---

## 💡 Key Takeaways

- Odor and CapColor are the most influential features  
- Decision Tree with proper tuning provides accurate and interpretable results  
- Cross-validation + statistical testing ensures robust model selection

---

## 👤 Author

**Surapot Nonpassopon**  
MSc Data Science and Analytics, University of Leeds  
📂 GitHub Portfolio: [github.com/surapotsrp](https://github.com/surapotsrp)
