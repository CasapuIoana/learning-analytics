
# COVID-19 Trends Analysis and Prediction

This repository contains a Jupyter notebook that analyzes and predicts trends in vaccination intent, vaccination rates, and side effect interest. It is designed as a **big data project**, leveraging **Google BigQuery** for scalable data storage and query capabilities, and **PySpark** for distributed data processing and machine learning. The notebook utilizes a public BigQuery dataset related to COVID-19.

## Features
- **Big Data Integration**: Uses BigQuery to access and query large datasets directly.
- **Data Cleaning and Transformation**: Handles missing values and normalizes features using PySpark.
- **Correlation Analysis**: Provides a heatmap of correlations between key features.
- **Regression Models**: Implements Linear Regression, Decision Tree, Random Forest, and Gradient-Boosted Trees to predict average vaccination rates.
- **Evaluation**: Calculates performance metrics (R², RMSE, and MSE) for each model.

## Prerequisites
Ensure you have the following dependencies installed before running the notebook:

- **Python 3.7 or later**
- **PySpark**
- **pandas**
- **matplotlib**
- **seaborn**
- **scikit-learn**
- **Google Cloud SDK** (for accessing BigQuery)

To install the dependencies, you can run:
```bash
pip install pyspark pandas matplotlib seaborn scikit-learn google-cloud-bigquery
```

You will also need to:
- Set up a Google Cloud project.
- Enable the BigQuery API.
- Authenticate using a service account key or the `gcloud auth application-default login` command.

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/CasapuIoana/learning-analytics.git
   ```
2. Navigate to the project directory:
   ```bash
   cd learning-analytics
   ```
3. Open the Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
4. Configure your BigQuery credentials and project details in the notebook.
5. Execute the cells sequentially to analyze the data and generate predictions.

## Dataset
This project utilizes a **public Google BigQuery dataset** that includes:
- Average vaccination intent
- Average vaccination rate
- Average interest in vaccine side effects
- Weekly and yearly data

The dataset provides insights into vaccination trends and public interest during the COVID-19 pandemic. Using BigQuery allows efficient querying of this large dataset.

## Results
The following table summarizes the performance of different regression models used in the project:

| Model                  | R² (%)      | RMSE       | MSE          |
|------------------------|-------------|------------|--------------|
| Linear Regression      | 76.52       | 610.23     | 372,384.52   |
| Decision Tree          | 95.15       | 277.33     | 76,910.90    |
| Random Forest          | 94.18       | 303.76     | 92,272.63    |
| Gradient-Boosted Trees | 99.47       | 91.82      | 8,430.54     |

Gradient-Boosted Trees achieved the highest R² (99.47%) and the lowest RMSE (91.82), indicating superior predictive performance compared to other models.

## Big Data Technologies
- **Google BigQuery**: Enables querying of large datasets efficiently.
- **PySpark**: Facilitates distributed data processing and machine learning.

## License
This project is open-source and available under the [MIT License](LICENSE).

## Contribution
Feel free to contribute to this project by creating issues or submitting pull requests.
