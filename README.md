# Machine Learning in Python: A Beginner Project Portfolio

![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white) ![Jupyter](https://img.shields.io/badge/Jupyter-Notebooks-F37626?logo=jupyter&logoColor=white) ![scikit--learn](https://img.shields.io/badge/scikit--learn-Machine%20Learning-F7931E?logo=scikitlearn&logoColor=white)

## Project Overview

This repository is a collection of practical machine learning notebooks created to explore core concepts in Python. It walks through classification, regression, end-to-end model development, and ensemble learning using familiar datasets and visual explanations.

The project is intended for students and beginners who want to see how machine learning workflows are put together: load data, explore it, prepare features, train models, evaluate results, and try predictions.

## Project Goals

- Practice core machine learning workflows with Python and scikit-learn.
- Compare classification and regression approaches.
- Explore model evaluation, cross-validation, and parameter tuning.
- Build familiarity with Jupyter notebooks and data visualization.

## Project Architecture

```text
machine-learning-project/
├── README.md
├── notebooks/
│   ├── Classification_example.ipynb
│   ├── End_to_End_ML.ipynb
│   ├── Ensemble_learning.ipynb
│   └── Regression_example.ipynb
└── datasets/
    └── california_housing.csv
```

The provided materials include `california_housing.csv`. The end-to-end notebook loads California Housing using scikit-learn, which may download the dataset when first run. The classification and rent notebooks also refer to `diabetes.csv` and `House_Rent_Dataset.csv`; add those files to `datasets/` if you intend to run those notebooks, or obtain them separately and update the notebook paths.

## Notebooks

| Notebook | Focus | Main techniques |
|---|---|---|
| `Classification_example.ipynb` | Diabetes outcome classification | EDA, Random Forest classifier, feature importance, cross-validation, precision, recall, F1, ROC/AUC, confusion matrix |
| `Regression_example.ipynb` | House rent prediction | One-hot encoding, Random Forest and Linear Regression, cross-validation, MSE/MAE, feature importance, prediction plots |
| `End_to_End_ML.ipynb` | California house-value regression | Data exploration, scaling, model comparison, grid search, RMSE, residuals, feature importance |
| `Ensemble_learning.ipynb` | Breast cancer classification | Bagging, Random Forest, Extra Trees, AdaBoost, Gradient Boosting, voting, and stacking |

## Technologies

- Python 3
- Jupyter Notebook
- NumPy and Pandas
- Matplotlib and Seaborn
- scikit-learn
- Google Colab, Visual Studio Code, or Anaconda/Jupyter for running notebooks

## How to Run

### Google Colab

1. Open [Google Colab](https://colab.research.google.com/).
2. Choose **File → Open notebook → GitHub** and provide the repository URL, or upload a notebook file.
3. For the classification and rent notebooks, place their CSV files in Google Drive under `MyDrive/pip-datasets/` to match the paths currently used in the notebooks.
4. Run notebook cells from top to bottom. If a package is missing, run:

   ```python
   %pip install numpy pandas matplotlib seaborn scikit-learn
   ```

### Visual Studio Code

1. Install [Python](https://www.python.org/downloads/) and [Visual Studio Code](https://code.visualstudio.com/).
2. Install Microsoft's **Python** and **Jupyter** extensions in VS Code.
3. Open the repository folder and then open a notebook.
4. Install dependencies in the selected Python environment:

   ```bash
   python -m pip install numpy pandas matplotlib seaborn scikit-learn jupyter
   ```

5. Select the notebook kernel and run cells in order. Update `pd.read_csv(...)` paths to your local dataset location, such as `../datasets/diabetes.csv` when notebooks are inside `notebooks/`.

See the [VS Code Jupyter guide](https://code.visualstudio.com/docs/datascience/jupyter-notebooks) for more information.

### Anaconda and Jupyter

1. Download Anaconda Distribution from the official [Anaconda download page](https://www.anaconda.com/download) and install it for your operating system.
2. Open Anaconda Navigator and launch JupyterLab or Jupyter Notebook.
3. Navigate to the project and open a notebook.
4. If required, install packages from Anaconda Prompt or a terminal:

   ```bash
   conda install numpy pandas matplotlib seaborn scikit-learn notebook
   ```

5. Update local CSV paths as needed, then run the cells in order.

## Notes for Reproducibility

- The CSV notebooks use Google Drive paths such as `/content/drive/MyDrive/pip-datasets/diabetes.csv`. Those paths need to be changed for local use.
- `Regression_example.ipynb` uses `OneHotEncoder(sparse=False)`. With newer scikit-learn releases, use `OneHotEncoder(sparse_output=False)` if the old argument is rejected.
- `End_to_End_ML.ipynb` uses `mean_squared_error(..., squared=False)`. In scikit-learn 1.6 and newer, use `root_mean_squared_error(y_test, y_test_pred)` instead.
- In the classification notebook, refit the classifier after the cross-validation cell before using it to predict the test set; the current cell sequence may otherwise raise a not-fitted error.
- Dataset availability and permissions vary. Confirm the source and redistribution terms for any dataset you add to a public repository.

## Author

**Shahadat Hossain**  
BSc in Computer Science and Engineering  
American International University-Bangladesh (AIUB)

> This project was done in Machine Learning Course in BSc Computer Science and Engineering AIUB by myself.

---

A personal academic project documenting my practical learning and application of machine learning concepts in Python.
