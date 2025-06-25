# Apple Price Prediction using Genetic Algorithm

Predict the stock price of Apple Inc. (AAPL) using a Genetic Algorithm (GA) to optimize a neural network for time series forecasting. This project demonstrates how evolutionary algorithms can be used for financial prediction tasks.

## Features
- Loads and preprocesses historical Apple stock data
- Builds a neural network whose weights are optimized using a genetic algorithm
- Evaluates model performance with standard metrics (MAE, MSE, RMSE, R²)
- Visualizes predictions and GA fitness over generations

## Dataset
- **File:** `HistoricalQuotes.csv`
- **Columns:**
  - Date
  - Close/Last
  - Volume
  - Open
  - High
  - Low

## Requirements
- Python 3.x
- pandas
- numpy
- matplotlib
- scikit-learn
- jupyter (for running the notebook)

Install dependencies with:
```bash
pip install pandas numpy matplotlib scikit-learn jupyter
```

## Setup & Usage
1. Clone or download this repository and ensure `HistoricalQuotes.csv` is in the project directory.
2. Start Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
3. Open `main.ipynb` and run all cells sequentially.

## How it Works
- The notebook preprocesses the data, creating lagged features for time series prediction.
- A simple feedforward neural network is defined, but its weights are not learned via backpropagation. Instead, a genetic algorithm evolves a population of candidate weight sets.
- The best set of weights (chromosome) is selected based on validation RMSE.
- The model's predictions are compared to actual prices, and results are visualized.

## Results
- The notebook prints evaluation metrics (MAE, MSE, RMSE, R²) on the test set.
- Plots show actual vs. predicted prices and the evolution of GA fitness over generations.

## License
This project is for educational purposes only. 