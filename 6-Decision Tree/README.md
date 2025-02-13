# Decision Tree Algorithm Repository

## Overview

This repository contains the implementation of a Decision Tree algorithm from scratch. The Decision Tree is a powerful and interpretable machine learning model used for both classification and regression tasks. This implementation includes all the core functionalities required to build, train, and evaluate a Decision Tree model.

## Features

- **Tree Construction**: Implements the recursive splitting of data based on feature values to build the decision tree.
- **Splitting Criteria**: Supports multiple splitting criteria such as:
  - **Gini Impurity** (for classification)
  - **Information Gain** (for classification)
  - **Variance Reduction** (for regression)
- **Pruning**: Includes pre-pruning (early stopping) and post-pruning techniques to avoid overfitting.
- **Handling Missing Values**: Implements strategies to handle missing data during training and prediction.
- **Feature Importance**: Calculates and provides feature importance scores based on the splits.
- **Visualization**: Includes functionality to visualize the decision tree structure.
- **Prediction**: Supports prediction on new data points using the trained decision tree.

## Repository Structure

```
decision-tree-repo/
├── ml/
│   ├── decision_tree.py       # Main implementation of the Decision Tree algorithm
│   ├── utils.py               # Utility functions for data preprocessing, splitting, etc.
│   ├── metrics.py             # Functions to calculate accuracy, MSE, etc.
│   └── visualization.py       # Functions to visualize the decision tree
├── datasets/                  # Sample datasets for testing
│   ├── classification.csv
│   └── regression.csv
├── examples/                  # Example scripts to demonstrate usage
│   ├── classification_example.py
│   └── regression_example.py
├── tests/                     # Unit tests for the Decision Tree implementation
│   ├── test_decision_tree.py
│   └── test_utils.py
└── README.md                  # This file
```

## Installation

To use this Decision Tree implementation, clone the repository and install the required dependencies:

```bash
git clone https://github.com/AbdulrahmanRagab/decision-tree-repo.git
cd decision-tree-repo
pip install -r requirements.txt
```


```python
from ml.visualization import plot_decision_tree

# Visualize the trained decision tree
plot_decision_tree(clf)
```

## Parameters

### DecisionTreeClassifier
- `criterion`: Splitting criterion (`"gini"` or `"information_gain"`).
- `max_depth`: Maximum depth of the tree.
- `min_samples_split`: Minimum number of samples required to split a node.
- `min_samples_leaf`: Minimum number of samples required at a leaf node.
- `max_features`: Maximum number of features to consider for splitting.
- `random_state`: Seed for random number generation.

### DecisionTreeRegressor
- `criterion`: Splitting criterion (`"variance_reduction"`).
- `max_depth`: Maximum depth of the tree.
- `min_samples_split`: Minimum number of samples required to split a node.
- `min_samples_leaf`: Minimum number of samples required at a leaf node.
- `max_features`: Maximum number of features to consider for splitting.
- `random_state`: Seed for random number generation.

## Testing

To run the unit tests, use the following command:

```bash
python -m pytest tests/
```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Feel free to explore the code and examples to understand how the Decision Tree algorithm works. If you have any questions or suggestions, please open an issue in the repository. Happy coding! 🚀
