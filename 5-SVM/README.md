# SVM Classification and Regression Repository

This repository provides a comprehensive guide and implementation of Support Vector Machines (SVM) for both classification and regression tasks. It includes a custom function, `svm_margin_plot`, which visualizes the decision boundaries and margins of an SVM model, making it easier to understand how the model separates different classes or predicts continuous values.

## Table of Contents
1. [Introduction](#introduction)
2. [Repository Structure](#repository-structure)
3. [Installation](#installation)
4. [Usage](#usage)
   - [Classification](#classification)
   - [Regression](#regression)
   - [Visualization with `svm_margin_plot`](#visualization-with-svm_margin_plot)
5. [Dependencies](#dependencies)
6. [Contributing](#contributing)
7. [License](#license)

---

## Introduction
Support Vector Machines (SVM) are powerful supervised learning algorithms used for both classification and regression tasks. This repository demonstrates how to implement SVM for these tasks using Python and provides a visualization tool (`svm_margin_plot`) to better understand the model's decision boundaries and margins.

---

## Repository Structure
```
svm-classification-regression/
├── data/                     # Directory containing sample datasets
├── notebooks/                # Jupyter notebooks with examples
├── scripts/                  # Python scripts for SVM implementation
│   ├── svm_classification.py
│   ├── svm_regression.py
│   └── svm_margin_plot.py    # Custom function for visualization
├── README.md                 # This file
└── requirements.txt          # List of dependencies
```

---

## Installation
To use this repository, clone it to your local machine and install the required dependencies.

```bash
# Clone the repository
git clone https://github.com/AbdulrahmanRagab/svm-classification-regression.git

# Navigate to the repository
cd svm-classification-regression

# Install dependencies
pip install -r requirements.txt
```

---

## Usage

### Classification
The `svm_classification.py` script demonstrates how to use SVM for classification tasks. It includes:
- Loading and preprocessing data.
- Training an SVM classifier.
- Evaluating the model using metrics like accuracy, precision, and recall.

### Regression
The `svm_regression.py` script demonstrates how to use SVM for regression tasks. It includes:
- Loading and preprocessing data.
- Training an SVM regressor.
- Evaluating the model using metrics like Mean Squared Error (MSE) and R² score.

### Visualization with `svm_margin_plot`
The `svm_margin_plot` function is a custom tool for visualizing the decision boundaries and margins of an SVM model. It is particularly useful for understanding how the model separates instances in classification tasks.

#### Example Usage:
```python
from scripts.svm_margin_plot import svm_margin_plot
from sklearn import datasets
from sklearn.svm import SVC

# Load dataset
X, y = datasets.make_classification(n_samples=100, n_features=2, n_informative=2, n_redundant=0, random_state=42)

# Train SVM classifier
model = SVC(kernel='linear')
model.fit(X, y)

# Plot decision boundaries and margins
svm_margin_plot(X, y, model)
```

---

## Dependencies
The following Python libraries are required to run the code in this repository:
- `numpy`
- `pandas`
- `scikit-learn`
- `matplotlib`
- `seaborn`

You can install all dependencies using the `requirements.txt` file:
```bash
pip install -r requirements.txt
```

---

## Contributing
Contributions are welcome! If you have suggestions, improvements, or new features to add, please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Commit your changes.
4. Submit a pull request with a detailed description of your changes.

---

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---
