# Random Forest Regression: Rock Density Prediction

## Project Overview

This project focuses on predicting rock density using signal strength data obtained from X-ray sensors. The goal is to help a tunnel boring company optimize their equipment by predicting rock density in advance, allowing them to switch boring heads efficiently. The dataset contains signal strength (in nHz) and corresponding rock density measurements. The relationship between signal strength and density appears oscillatory, resembling a sine wave, which makes this an interesting regression problem.

The project explores various regression techniques, including Linear Regression, Polynomial Regression, K-Nearest Neighbors (KNN), Decision Trees, Support Vector Regression (SVR), Random Forest Regression, and ensemble methods like Voting Regressor, AdaBoost, and Gradient Boosting. The performance of each model is evaluated using Root Mean Squared Error (RMSE).

---

## Table of Contents

1. [Features](#features)
2. [Technologies Used](#technologies-used)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Results](#results)
6. [Contributing](#contributing)
7. [License](#license)
8. [Credits](#credits)

---

## Features

- **Data Exploration**: Visualizes the relationship between signal strength and rock density using scatter plots.
- **Multiple Regression Models**: Implements and compares various regression models:
  - Linear Regression
  - Polynomial Regression
  - K-Nearest Neighbors (KNN)
  - Decision Tree Regression
  - Support Vector Regression (SVR)
  - Random Forest Regression
  - Ensemble Methods (Voting Regressor, AdaBoost, Gradient Boosting)
- **Model Evaluation**: Evaluates models using RMSE and visualizes predictions.
- **Early Stopping**: Implements early stopping for Gradient Boosting to prevent overfitting.
- **Optimal Model Selection**: Identifies the best number of estimators for Gradient Boosting using validation error.

---

## Technologies Used

- **Programming Language**: Python
- **Libraries**:
  - `NumPy`, `Pandas` for data manipulation
  - `Matplotlib`, `Seaborn` for data visualization
  - `Scikit-learn` for machine learning models and evaluation
- **Machine Learning Models**:
  - Linear Regression, Polynomial Regression, KNN, Decision Trees, SVR, Random Forest, AdaBoost, Gradient Boosting, Voting Regressor

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/AbdulrahmanRagab/rock-density-prediction.git
   cd rock-density-prediction
   ```

2. Install the required dependencies:
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn
   ```

3. Download the dataset (`rock_density_xray.csv`) and place it in the appropriate directory.

---

## Usage

1. Open the Jupyter Notebook or Python script provided in the repository.
2. Run the code to load the dataset, preprocess the data, and train the models.
3. Evaluate the models using RMSE and visualize the predictions.
4. Use the best-performing model (e.g., Gradient Boosting with early stopping) for rock density prediction.

Example code snippet:
```python
from sklearn.ensemble import GradientBoostingRegressor
from sklearn.metrics import mean_squared_error

# Train the Gradient Boosting model
gbrt = GradientBoostingRegressor(max_depth=2, n_estimators=120)
gbrt.fit(x_train, y_train)

# Evaluate the model
y_pred = gbrt.predict(x_test)
rmse = np.sqrt(mean_squared_error(y_test, y_pred))
print(f"RMSE: {rmse}")
```

---

## Results

- **Best Model**: Gradient Boosting with early stopping achieved the lowest RMSE.
- **Optimal Number of Estimators**: Identified using validation error.
- **Visualization**: Predictions are visualized alongside the actual data to assess model performance.


---

## Contributing

Contributions are welcome! If you'd like to contribute, please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Commit your changes.
4. Submit a pull request with a detailed description of your changes.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Credits

- **Dataset**: Provided by a tunnel boring company.
- **Libraries**: Thanks to the developers of `NumPy`, `Pandas`, `Matplotlib`, `Seaborn`, and `Scikit-learn`.
- **Inspiration**: The oscillatory relationship between signal strength and rock density inspired this project.

---
