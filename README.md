# 🏀 College Basketball Defense Analysis
**Language:** R  
**Focus:** Machine Learning, Data Analytics  

## 📊 Overview
This project analyzes how defensive performance influences NCAA tournament selection for Division I men's basketball teams.  
Using a Kaggle dataset, I performed exploratory data analysis (EDA), feature engineering, and predictive modeling to evaluate the role of defensive efficiency.

## ⚙️ Data Source
Dataset: [College Basketball Dataset – Kaggle](https://www.kaggle.com/datasets/andrewsundberg/college-basketball-dataset)  
Includes statistics such as:
- Adjusted Defensive Efficiency (`ADJDE`)
- Effective Field Goal % Allowed (`EFG_D`)
- Defensive Rebound Rate (`DRB`)
- Two-Point % Allowed (`X2P_D`)
- Tournament Seed (`SEED`)

## 🧠 Methodology
1. Cleaned and prepared the dataset in R.  
2. Created a new binary variable `made_tourney` to label teams as “Made” or “Not_Made”.  
3. Split data into **training (80%)** and **testing (20%)** sets.  
4. Trained and evaluated two models:
   - `rpart()` Decision Tree  
   - Naïve Bayes (using `e1071` package)
5. Compared model performance using confusion matrices.

## 🧩 Tools & Libraries
- **R**
- **caret** – model evaluation  
- **e1071** – Naïve Bayes classification  
- **rpart** / **rpart.plot** – decision tree modeling and visualization  
- **ggplot2** – data visualization  

## 📈 Results
- **Decision Tree Accuracy:** ~0.86  
- **Naïve Bayes Accuracy:** ~0.81  
- Teams with **ADJDE < 98** (better defense) had the highest probability of making the tournament.  
- Visualization confirmed a strong negative correlation between poor defensive metrics and tournament seeding.

| Model | Accuracy | Key Metric |
|--------|-----------|-------------|
| Decision Tree | 0.86 | ADJDE threshold: 98 |
| Naïve Bayes | 0.81 | EFG_D as secondary factor |

## 📊 Example Output
### Decision Tree
![Decision Tree Output](output/decision_tree.png)

### Confusion Matrix (Decision Tree)
![Confusion Matrix - Tree](output/confusion_matrix_tree.png)

## 💡 Lessons Learned
- Gained experience with **R machine learning workflows** and **model evaluation**.  
- Strengthened understanding of **feature selection** and **classification performance metrics**.  
- Reinforced the importance of data preprocessing and variable scaling for accuracy.

## 🧑‍💻 Author
**Anthony Rahner**  
B.S. Computer Science | Minor in Data Science  
Rutgers University – New Brunswick  
[GitHub](https://github.com/AnthonyRahner) • [LinkedIn](https://linkedin.com/in/anthonyrahner)
