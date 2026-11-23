# 🎓 Student Pass/Fail Prediction using Logistic Regression

A beginner-friendly machine learning project that predicts whether a student will **pass or fail** based on study habits, attendance, previous marks, and background details, using **Logistic Regression** in Python (scikit-learn).

---

## 📌 Project Overview

Logistic Regression is a classification algorithm used when the target has two outcomes. In this project, the target is **Result** (`1` = Pass, `0` = Fail). The notebook walks through a complete, simple ML workflow: loading data, cleaning, encoding categorical features, splitting data, training a model, and evaluating it.

## 📂 Repository Structure

```
├── Logistic_regression_Class_Practice.ipynb          # Main notebook (step-by-step code)
├── Student_Pass_Fail_Logistic_Regression_Dataset.csv  # Dataset (120 students)
└── README.md
```

## 📊 Dataset Description

The dataset contains **120 student records** with **10 columns**:

| Column | Type | Description |
|---|---|---|
| `Student_ID` | String | Unique student ID (dropped before training) |
| `Study_Hours_Per_Day` | Float | Average daily study hours |
| `Attendance_Percent` | Integer | Class attendance percentage |
| `Previous_Marks` | Integer | Marks scored in earlier exams |
| `Sleep_Hours` | Float | Average daily sleep hours |
| `Gender` | Categorical | Male / Female |
| `Study_Mode` | Categorical | Self Study / Group Study / Online |
| `Parent_Education` | Categorical | School / Graduate / Postgraduate |
| `Internet_Access` | Categorical | Yes / No |
| `Pass` | Binary (Target) | 1 = Pass, 0 = Fail (renamed to `Result` in the notebook) |

About 72.5% of the students in the dataset passed, so the classes are moderately imbalanced.

## 🔄 Workflow

1. **Import libraries**: NumPy, Pandas, Matplotlib, Seaborn, scikit-learn
2. **Load data** and inspect it (`head`, `info`, `dtypes`, `isnull`)
3. **Data cleaning**: rename `Pass` → `Result`, drop `Student_ID`, check missing values
4. **Explore categorical columns** with `unique()`
5. **Split features (X) and target (y)**
6. **Encode categorical variables** using `LabelEncoder` and `pd.get_dummies(drop_first=True)`
7. **Train/test split**: 70% train, 30% test (`random_state=42`)
8. **Train** a `LogisticRegression(max_iter=1000)` model
9. **Predict** on the test set
10. **Evaluate** using accuracy score

## 🛠️ Technologies Used

- Python 3
- NumPy
- Pandas
- Matplotlib
- Seaborn
- scikit-learn
- Jupyter Notebook

## 🚀 How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
   cd <repo-name>
   ```

2. **Install dependencies**
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn jupyter
   ```

3. **Launch the notebook**
   ```bash
   jupyter notebook Logistic_regression_Class_Practice.ipynb
   ```

4. Run all cells from top to bottom. Make sure the CSV file is in the same folder as the notebook.

## 📈 Results

The model reaches roughly **80% accuracy** on the test set (30% of the data). Exact numbers may vary slightly with library versions.

## 🔮 Future Improvements

- Add a confusion matrix, precision, recall, and F1-score
- Scale numeric features with `StandardScaler`
- Use cross-validation for a more reliable estimate on a small dataset
- Visualize feature importance (model coefficients)
- Compare with other models (Decision Tree, Random Forest, KNN)
- Collect more data to reduce overfitting risk

## 📚 What I Learned

- Handling categorical data with label encoding and one-hot encoding
- Splitting data for training and testing
- Building and evaluating a Logistic Regression classifier

## 👤 Author

**Shobana C**
GitHub: https://github.com/shobanachandran24-lab

## 📄 License

This project is open source and available under the Kaggle.
