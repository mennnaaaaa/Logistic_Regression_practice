# Logistic Regression Practice

A personal collection of machine learning practice projects focused on **Logistic Regression** and binary classification. These projects were completed while learning through courses, tutorials, and different learning resources. They are not presented as a single university assignment.

The repository moves from a small introductory example to applied classification work using advertising and Titanic datasets.

## Repository Overview

The projects explore how Logistic Regression can be used to solve binary classification problems in different contexts:

- Predicting whether a user will click an advertisement
- Predicting whether a Titanic passenger survived
- Understanding the basic training process on a simple binary dataset

The current repository contains three Jupyter notebooks and three CSV datasets at the root level. citerepo_contents

## Project Structure

```text
Logistic_Regression_practice/
├── 02-Logistic Regression Project.ipynb
├── Logistic_regression.ipynb
├── Logistic_Regression_titanic.ipynb
├── advertising.csv
├── titanic_train.csv
└── titanic_test.csv
```

## Project Files

| File | Type | Description | Main Algorithm / Method |
|---|---|---|---|
| `Logistic_regression.ipynb` | Jupyter Notebook | Introductory binary-classification example using a small manually created dataset. | `sklearn.linear_model.LogisticRegression` |
| `02-Logistic Regression Project.ipynb` | Jupyter Notebook | Applied classification project built around the advertising dataset. | Logistic Regression |
| `Logistic_Regression_titanic.ipynb` | Jupyter Notebook | Titanic survival classification workflow using passenger data. | Logistic Regression |
| `advertising.csv` | Dataset | User and advertising attributes with `Clicked on Ad` as the binary target. | Input data for advertising project |
| `titanic_train.csv` | Dataset | Titanic training data containing the `Survived` target and passenger attributes. | Training data |
| `titanic_test.csv` | Dataset | Titanic test data used with the Titanic workflow. | Test / prediction data |

## 1. Logistic Regression Basics

### File
`Logistic_regression.ipynb`

### Objective

This notebook introduces the basic workflow for training a Logistic Regression classifier with scikit-learn.

The example creates a small binary dataset:

```python
x = np.array([[1], [2], [3], [4]])
y = np.array([0, 0, 1, 1])
```

The model is then created and fitted:

```python
model = LogisticRegression()
model.fit(x, y)
```

The source notebook explicitly imports `LogisticRegression` from `sklearn.linear_model` and uses it to fit the example data. citebasic_notebook

### Algorithm

**Binary Logistic Regression**

Logistic Regression is a supervised learning algorithm used for binary classification. It estimates the probability of the positive class and can then convert that probability into a class prediction using a decision threshold. citelogistic_regression_reference

### Learning Focus

This notebook provides the foundation for understanding the estimator before applying the same algorithm to larger datasets.

## 2. Advertising Click Prediction

### Files

- `02-Logistic Regression Project.ipynb`
- `advertising.csv`

### Objective

This project applies Logistic Regression to an advertising dataset with `Clicked on Ad` as the target variable.

The CSV contains fields including:

- `Daily Time Spent on Site`
- `Age`
- `Area Income`
- `Daily Internet Usage`
- `Ad Topic Line`
- `City`
- `Male`
- `Country`
- `Timestamp`
- `Clicked on Ad`

These columns are present directly in the repository dataset. citeadvertising_data

### Application

The project represents a **digital advertising engagement prediction** problem. The classification task is to estimate whether a user will click an advertisement.

This type of problem can be connected to real-world machine learning use cases such as:

- Advertising campaign analysis
- Customer engagement prediction
- Audience segmentation
- Click-through prediction
- Personalization and targeting workflows

The broader idea is to use user-level features to estimate the probability of a binary behavior. citelogistic_regression_reference

### Algorithm

**Logistic Regression** is the main classification algorithm represented in this project.

## 3. Titanic Survival Prediction

### Files

- `Logistic_Regression_titanic.ipynb`
- `titanic_train.csv`
- `titanic_test.csv`

### Objective

This project applies Logistic Regression to the Titanic dataset to predict the binary target `Survived`.

The notebook loads the training dataset with:

```python
train = pd.read_csv('titanic_train.csv')
```

It imports Pandas, NumPy, Matplotlib, and Seaborn for data loading, inspection, and visualization. citetitanic_notebook

The training data includes:

- `PassengerId`
- `Survived`
- `Pclass`
- `Name`
- `Sex`
- `Age`
- `SibSp`
- `Parch`
- `Ticket`
- `Fare`
- `Cabin`
- `Embarked`

These fields are present in the repository's Titanic training dataset. citetitanic_data

### Application

The project demonstrates **binary event prediction from structured passenger data**.

As a machine learning exercise, it provides practice with:

- Exploratory Data Analysis
- Structured tabular data
- Feature preparation
- Binary classification
- Model training
- Prediction and interpretation

### Algorithm

**Logistic Regression** is the core classification method used for the Titanic problem.

## Algorithms Covered

### Logistic Regression

Logistic Regression is the central algorithm throughout the repository.

For binary classification, the model applies the logistic sigmoid function to a linear combination of input features to obtain a probability between 0 and 1. A decision threshold can then be used to produce a binary prediction. citelogistic_regression_reference

The repository demonstrates the algorithm at three practical levels:

1. A minimal synthetic example.
2. An advertising engagement problem.
3. A Titanic survival classification problem.

The introductory notebook uses `sklearn.linear_model.LogisticRegression`. citebasic_notebook

## Machine Learning Workflow

The projects follow the general pattern below, with exact preprocessing and evaluation depending on the notebook:

```text
Dataset
   |
   v
Data Loading
   |
   v
Exploration
   |
   v
Feature Preparation
   |
   v
Logistic Regression
   |
   v
Prediction
   |
   v
Evaluation / Interpretation
```

For example, the Titanic notebook explicitly loads the CSV and displays the beginning of the training data before continuing with the analysis. citetitanic_notebook

## Technologies

- Python
- Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

## Installation

```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

## How to Run

Clone the repository:

```bash
git clone https://github.com/mennnaaaaa/Logistic_Regression_practice.git
cd Logistic_Regression_practice
```

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open any notebook and run the cells in sequence.

Keep the CSV files in the same directory as the notebooks because the notebooks use local relative paths such as `titanic_train.csv`.

## Learning Outcomes

This collection demonstrates practical experience with:

- Binary classification
- Logistic Regression model creation
- NumPy arrays and Pandas DataFrames
- Dataset inspection and exploratory analysis
- Applying one classification algorithm to multiple domains
- Connecting machine learning methods to practical prediction problems
- Building a foundation for more advanced supervised learning algorithms

## Practical Applications Represented

### Advertising

Predicting ad-click behavior provides an example of user-engagement modeling in digital advertising.

### Survival Classification

Predicting the `Survived` outcome provides an example of binary event classification using structured passenger information.

These projects demonstrate how the same core algorithm can be adapted to different datasets and application contexts.

## Project Background

This repository is a personal learning collection developed through courses, tutorials, and different learning resources. It is not a single university project. The notebooks represent hands-on practice with Logistic Regression, starting with a minimal example and progressing to applied classification datasets.

## Future Development

Potential extensions include:

- Consistent reporting of accuracy, precision, recall, F1-score, ROC-AUC, and confusion matrices
- Cross-validation for more robust model assessment
- Reusable preprocessing pipelines
- Hyperparameter tuning and regularization experiments
- Comparison with Decision Trees, Random Forests, SVM, and other classifiers
- Separate Python scripts in addition to notebooks
- A dedicated `requirements.txt` file
- More structured folders for notebooks and datasets as the collection grows

## Author

**Menna Hany Abdelaziz**

GitHub: [mennnaaaaa](https://github.com/mennnaaaaa)

Repository: [Logistic_Regression_practice](https://github.com/mennnaaaaa/Logistic_Regression_practice)

## References

- Scikit-learn documentation for Logistic Regression
- The notebooks and datasets contained in this repository
- Standard machine learning references on binary classification
