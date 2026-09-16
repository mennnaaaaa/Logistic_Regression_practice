# Logistic Regression Practice

A collection of machine learning practice projects focused on **Logistic Regression** and binary classification. This repository brings together projects completed while learning from courses, tutorials, and different learning resources rather than as a single university assignment.

The work covers both a small introductory classification example and practical applications using advertising and Titanic datasets. The notebooks document the process of loading data, exploring it, preparing features, fitting classification models, and examining predictions.

## Repository Overview

The main purpose of this repository is to build practical understanding of Logistic Regression by applying the algorithm to different datasets and problem settings.

The projects demonstrate how a classification model can be used to answer questions such as:

- Will a user click on an online advertisement?
- Is a passenger predicted to survive based on available passenger information?
- How does a basic Logistic Regression model behave on a simple binary dataset?

## Project Files

| File | Type | Description | Main Algorithm / Method |
|---|---|---|---|
| `Logistic_regression.ipynb` | Jupyter Notebook | Introductory Logistic Regression example using a small manually created dataset. | `sklearn.linear_model.LogisticRegression` |
| `02-Logistic Regression Project.ipynb` | Jupyter Notebook | Practical classification project built around the advertising dataset. | Logistic Regression |
| `Logistic_Regression_titanic.ipynb` | Jupyter Notebook | Titanic survival classification workflow using passenger data. | Logistic Regression |
| `advertising.csv` | Dataset | Advertising-user data with a binary `Clicked on Ad` target. | Used by advertising classification work |
| `titanic_train.csv` | Dataset | Titanic training data containing the `Survived` target and passenger attributes. | Used for model training |
| `titanic_test.csv` | Dataset | Titanic test data used with the Titanic workflow. | Used for model evaluation/prediction |

The repository currently contains three notebooks and three dataset files at the root level. This structure is verified against the current GitHub repository contents. citerepo_contents

## 1. Logistic Regression Basics

### File
`Logistic_regression.ipynb`

### Objective
This notebook is a compact introduction to training a Logistic Regression classifier with scikit-learn.

The notebook creates a very small dataset:

```python
x = np.array([[1], [2], [3], [4]])
y = np.array([0, 0, 1, 1])
```

It then creates and fits the model with:

```python
model = LogisticRegression()
model.fit(x, y)
```

This project focuses on understanding the basic model-training workflow: defining input features and binary labels, creating the estimator, and fitting it to the data. The actual notebook uses `LogisticRegression` from scikit-learn. citebasic_notebook

### Algorithm
**Binary Logistic Regression**

Logistic Regression is a supervised learning algorithm used to model the probability of a binary outcome. It is particularly useful when the prediction target has two classes, such as 0/1. citelogistic_regression_reference

### Learning Value
This notebook serves as a foundation for understanding the same algorithm before applying it to larger and more realistic datasets.

## 2. Advertising Click Prediction

### Files
- `02-Logistic Regression Project.ipynb`
- `advertising.csv`

### Objective
This project applies Logistic Regression to an advertising dataset where the target variable is `Clicked on Ad`. The dataset includes user and browsing attributes such as:

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

The dataset structure is present directly in the repository. citeadvertising_data

### Application
The project represents a practical **digital advertising classification** problem: using available user information to predict whether a person will click an advertisement.

This type of prediction is relevant to areas such as:

- Online advertising and campaign analysis
- Customer engagement prediction
- Marketing segmentation
- Click-through-rate modeling
- Personalization and recommendation workflows

These are examples of how binary classification can support decisions around user engagement and marketing behavior. Logistic Regression is commonly used for binary probability modeling in applications of this kind. citelogistic_regression_reference

### Algorithm
**Logistic Regression** is the primary classification algorithm represented in this project.

The general modeling idea is to estimate the probability of the positive class and convert that probability into a binary prediction using a decision threshold.

## 3. Titanic Survival Prediction

### Files
- `Logistic_Regression_titanic.ipynb`
- `titanic_train.csv`
- `titanic_test.csv`

### Objective
This project applies Logistic Regression to the Titanic dataset to predict the binary target `Survived`.

The notebook loads the training data with:

```python
train = pd.read_csv('titanic_train.csv')
```

The dataset contains passenger information including:

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

The notebook also uses NumPy, Pandas, Matplotlib, and Seaborn for data handling and visualization. citetitanic_notebook

### Application
The project demonstrates **binary outcome prediction from structured passenger data**.

From a machine learning perspective, this type of workflow is useful for learning how demographic and travel-related variables can be transformed into model features and used to estimate the probability of a binary event.

The Titanic dataset is especially useful for practicing:

- Exploratory Data Analysis
- Missing-value handling
- Categorical feature preparation
- Binary classification
- Model evaluation
- Interpretation of classification results

### Algorithm
**Logistic Regression** is used as the core classification approach.

The problem is naturally binary because the target represents two outcomes: survived or did not survive.

## Algorithms Covered in This Repository

### Logistic Regression
The main algorithm across the repository is Logistic Regression.

At a high level, the algorithm models a linear combination of input features and passes it through the logistic sigmoid function to obtain a probability between 0 and 1. A classification threshold can then be used to map the probability to a class label. citelogistic_regression_reference

The repository demonstrates the algorithm at multiple levels:

1. A very small synthetic example for understanding the estimator.
2. An advertising classification problem.
3. A Titanic survival classification problem.

The scikit-learn implementation used in the introductory notebook is `sklearn.linear_model.LogisticRegression`. citebasic_notebook

## Data Science Workflow Practiced

Across the projects, the repository supports a practical learning workflow:

```text
Dataset
   |
   v
Data Loading
   |
   v
Exploration and Inspection
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
Evaluation and Interpretation
```

The exact preprocessing and evaluation steps depend on the notebook. The Titanic notebook, for example, visibly includes data loading and exploratory inspection before the classification work. citetitanic_notebook

## Technologies

- Python
- Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

## Installation

Install the main dependencies with:

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

Then open any of the notebooks and run the cells in order.

Keep the CSV files in the same directory as the notebooks so that the relative file paths used by the projects continue to work.

## Learning Outcomes

Through these projects, the following skills are practiced:

- Understanding the purpose of Logistic Regression
- Working with binary classification problems
- Creating models with scikit-learn
- Loading and inspecting real datasets
- Working with structured tabular data
- Connecting machine learning algorithms to practical applications
- Comparing the same classification algorithm across different datasets
- Building a foundation for more advanced machine learning models

## Applications Represented

The repository connects Logistic Regression to two practical problem types.

### Advertising Engagement
Predicting whether a user will click an advertisement is a classification task that can support marketing analysis and user-engagement modeling.

### Survival Classification
Predicting the `Survived` outcome demonstrates how a machine learning model can classify a binary event from passenger characteristics.

Together, these projects show that the same core algorithm can be reused for different domains as long as the problem can be framed as binary classification.

## Project Background

This repository is a personal learning collection built through practice with courses, tutorials, and multiple learning resources. It is not presented as a single university course project. The notebooks represent progressive practice with Logistic Regression, from a minimal example to applied classification projects.

## Limitations and Future Development

Potential extensions to this repository include:

- Adding train/validation/test comparisons where appropriate
- Reporting precision, recall, F1-score, and ROC-AUC alongside accuracy
- Applying cross-validation for more robust evaluation
- Comparing Logistic Regression with Decision Trees, Random Forests, and Support Vector Machines
- Adding feature scaling and systematic preprocessing pipelines
- Tuning regularization and other model hyperparameters
- Creating reusable Python scripts in addition to notebooks
- Adding a dedicated `requirements.txt` file
- Organizing datasets, notebooks, and documentation into separate directories as the collection grows

## Author

**Menna Hany Abdelaziz**

GitHub: [mennnaaaaa](https://github.com/mennnaaaaa)

Repository: [Logistic_Regression_practice](https://github.com/mennnaaaaa/Logistic_Regression_practice)
