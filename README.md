# Bike Rental Data Analysis

This project analyzes daily bike rental data to uncover trends, seasonality, and build a simple forecasting model. The analysis is performed in a Jupyter Notebook using Python, pandas, matplotlib, seaborn, and statsmodels.

## Dataset

- **Source:** [Kaggle - Bike Sharing Dataset](https://www.kaggle.com/datasets/archit9406/bike-sharing)
- **File:** `day.csv` (download from the link above)
- **Description:** Contains daily records of bike rentals, weather, and calendar information.
- **Columns:**
  - `instant`: Record index
  - `dteday`: Date
  - `season`: Season (1=spring, 2=summer, 3=fall, 4=winter)
  - `yr`: Year (0=2011, 1=2012)
  - `mnth`: Month (1 to 12)
  - `holiday`: Whether the day is a holiday
  - `weekday`: Day of the week (0=Sunday)
  - `workingday`: If day is neither weekend nor holiday
  - `weathersit`: Weather situation
  - `temp`, `atemp`: Normalized temperature
  - `hum`: Normalized humidity
  - `windspeed`: Normalized wind speed
  - `casual`: Count of casual users
  - `registered`: Count of registered users
  - `cnt`: Total count of rentals (target variable)

## Project Structure

- [`main.ipynb`](main.ipynb): Jupyter Notebook with all analysis, visualizations, and modeling.
- `day.csv`: The dataset (download from Kaggle and place in this directory).
- `.gitignore`: Standard Python and Jupyter ignore rules.

## Analysis Steps

1. **Data Loading & Inspection**
   - Load the dataset and inspect structure, types, and summary statistics.

2. **Preprocessing**
   - Convert date columns, set index, and select relevant features.

3. **Exploratory Data Analysis (EDA)**
   - Visualize trends, seasonality, and the impact of features like season and weekday on rentals.

4. **Time Series Decomposition**
   - Decompose the rental count into trend, seasonality, and residuals.

5. **Forecasting**
   - Split data into training and testing sets.
   - Fit a SARIMAX (ARIMA) model for forecasting.
   - Evaluate model performance using MAE and RMSE.
   - Visualize actual vs. forecasted rentals with confidence intervals.

## How to Run

1. **Install dependencies** (recommended: use a virtual environment):

   ```sh
   pip install numpy pandas matplotlib seaborn statsmodels scikit-learn
   ```

2. **Download `day.csv` from [Kaggle](https://www.kaggle.com/datasets/archit9406/bike-sharing) and place it in the project directory.**

3. **Open `main.ipynb` in Jupyter Notebook or VS Code and run the cells sequentially.**

## Results

- Visualizations of rental trends, seasonality, and feature impacts.
- Model summary and forecast accuracy metrics.
- Plots comparing actual and predicted rentals.

## License

This project is for educational and research purposes.

---

*Feel free to explore and modify the notebook for deeper insights or improved