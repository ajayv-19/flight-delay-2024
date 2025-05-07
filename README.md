# ✈️ Flight Delay Prediction Using Big Data

## 📌 Overview

Flight delays are a persistent challenge in the aviation industry, leading to financial losses, customer dissatisfaction, and operational inefficiencies. This project leverages Big Data technologies to build a scalable machine learning pipeline that predicts flight delays and generates actionable insights. Using historical flight data from the Bureau of Transportation Statistics (BTS), the project utilizes Hadoop HDFS for distributed storage, PySpark and MLlib for processing and modeling, and visualization libraries like Seaborn, Matplotlib, and Plotly for data exploration and presentation.

---

## 🛠️ Technologies Used

- **Dataset**: [BTS - Bureau of Transportation Statistics](https://www.transtats.bts.gov/)
- **Storage**: Hadoop HDFS
- **Processing**: Apache Spark, PySpark, Spark SQL
- **Machine Learning**: PySpark MLlib
- **Visualization**: Seaborn, Matplotlib, Plotly
- **Environment**: Jupyter Notebook, Google Colab, Dataproc


## 📂 Project Structure
- Dataset - 2024 airline delay dataset from BTS
- airports.dat
- Project Report - Final Report of our project
- Python Notebook - Main Notebook 
- ReadME - Project Documentation

## Code Execution Instructions
- To run this project and reproduce the results, follow the steps below:
### 1. Clone the Repository
```bash
git clone https://github.com/ajayvenkatesh19/flight-delay-2024.git
```
### 2. Set up Spark and Hadoop 
- Ensure Hadoop and Apache Spark are installed and configured
- Add them to your System Path
- In our case, we used Dataproc
- Create a Folder and transfer all the datasets into DataProc
  ```bash
  mkdir -p ~/flight_project_2024
  cd flight_project_2024
  ```
  ```bash
  head -n 1 2024_1.csv > full_2024.csv
  tail -n +2 -q 2024_*.csv >> full_2024.csv
  ```
- Upload to HDFS:
  ```bash
  hdfs dfs -mkdir -p /user/user_id/flight_data_2024
  hdfs dfs -put -f full_2024.csv /user/user_id/flight_data_2024/
  ```
- Launch Jupyter Notebook inside the folder and upload the notebook
  ```bash
  jupyter notebook --no-browser --port=8888
  ```
---

## 🚀 Features

- 📦 Distributed data ingestion from BTS and storage on HDFS  
- 🧹 Data cleaning, standardization, and feature engineering using PySpark  
- 🤖 Multiclass classification model to predict:
  - No Delay  
  - Delay ≤ 30 minutes  
  - Delay > 30 minutes  
  - Cancelled  
- 📊 Exploratory analysis by airport, route, time, airline, and weather
- 🧠 Insights for airline decision-makers and airport operations

---

## 📈 Visualizations

- Delay trends by route and airport
- Seasonal and time-of-day delay heatmaps
- Airline performance comparison
- Interactive dashboards with Plotly

---

## 🏗️ Architecture

This project follows a Big Data pipeline architecture:
1. **Data Ingestion** → BTS → HDFS  
2. **Processing** → PySpark  
3. **ML Modeling** → MLlib (Random Forest/Decision Tree / Logistic Regression / Multilayer Perceptron)  
4. **Visualization** → Seaborn / Matplotlib / Plotly  
5. **Output** → Predictions & dashboards

---

## 🔮 Future Scope

- Real-time data integration (live weather, traffic)
- Deep learning models for higher accuracy
- Integration with airline/airport APIs

---

## 📄 License

This project is licensed under the MIT License.

---
