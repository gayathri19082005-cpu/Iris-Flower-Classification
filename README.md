# Iris Flower Classification

**Oasis Infobyte — Data Science Internship, Task 1**

A beginner-friendly, end-to-end machine learning project that classifies Iris flowers into
one of three species — **Setosa**, **Versicolor**, or **Virginica** — based on four physical
measurements (sepal length, sepal width, petal length, petal width).

## Project Structure

```
Iris-Flower-Classification/
├── iris_classification.ipynb   # Main notebook — full analysis, visualizations, models
├── README.md                   # This file
├── requirements.txt            # Python dependencies
└── .gitignore
```

## Objective

Build and compare machine learning models that predict the species of an Iris flower from
its measurements, following a complete data science workflow: data loading, exploratory
data analysis, visualization, feature selection, model training, and evaluation.

## Dataset

The classic Iris dataset, loaded directly from `sklearn.datasets.load_iris()` — no external
file download required. It contains 150 samples, 50 for each of the three species, with four
numeric features per sample.

## Technologies Used

- Python 3
- Pandas & NumPy
- Scikit-learn
- Matplotlib & Seaborn
- Jupyter Notebook

## What the Notebook Covers

1. Project title, problem statement, and objective
2. Library imports
3. Loading the dataset into a Pandas DataFrame with meaningful column names
4. Understanding the dataset (shape, data types, descriptive statistics, class distribution)
5. Missing value / duplicate check
6. Exploratory data analysis
7. Visualizations: class distribution bar chart, pairplot, and box plots (with explanations
   after each one)
8. Feature selection with reasoning
9. 80/20 train-test split (`random_state=42` for reproducibility)
10. Training three models: **Logistic Regression**, **K-Nearest Neighbors**, and
    **Random Forest**
11. Evaluation with accuracy, precision, recall, F1-score, classification reports, and
    confusion matrix heatmaps
12. A model comparison table and chart
13. Final conclusion

## Results

On the held-out 20% test set (30 samples), the models achieved:

| Model                | Accuracy | Precision (macro) | Recall (macro) | F1-score (macro) |
|-----------------------|----------|--------------------|-----------------|--------------------|
| Logistic Regression   | 0.933    | 0.933              | 0.933           | 0.933              |
| K-Nearest Neighbors   | 0.933    | 0.944              | 0.933           | 0.933              |
| Random Forest         | 0.900    | 0.902              | 0.900           | 0.900              |

All three models classify **Setosa** with perfect accuracy in every run, since it is
linearly separable from the other two species. The small number of misclassifications that
occur are all between **Versicolor** and **Virginica**, which show some overlap in petal
measurements. Logistic Regression and KNN were the top performers on this test split; see
the notebook's Model Comparison section for the full reasoning.

*(Re-running the notebook will reproduce these exact numbers, since the train-test split
uses a fixed `random_state`.)*

## How to Run

1. Clone this repository / download the project folder.
2. (Recommended) Create and activate a virtual environment:
   ```bash
   python3 -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```
3. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
5. Open `iris_classification.ipynb` and run all cells (**Cell → Run All**). The notebook
   runs top-to-bottom without errors and needs no external data files — the dataset is
   loaded directly from scikit-learn.

## Author

Gayathri S
B.Tech CSE, SRM Institute of Science and Technology, Tiruchirappalli
