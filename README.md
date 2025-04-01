# Scalable-Sentiment-Analysis-Pipeline

## Project Overview:
In this project, I designed an End-to-End Data Pipeline for Scalable Sentiment Analysis to Predict and Visualize Customer Sentiments Using a Trained Machine Learning Model

### Data Ingestion:

OLTP Data: Users, Business, Checkin and Tips tables are extracted from the  OLTP database (RDS) and loaded into ADLS using using Azure Data Factory. This process is scheduled to run weekly .

Data lake  Data: Reviews is  collected from blob storage  and loaded into ADLS using Azure Data Factory . This  is orchestrated to run daily to receive the  yelp reviews

### Model training: 
Training data is ingesting from ADLS into Databricks and Model is trained using Logistic Regression. The model is saved as inference into ADLS 

### Predictions:
The saved model is included in our data pipeline to predict sentiments of the Reviews Data. The prediction is saved in another ADLS

### Data Visualization: 
The prediction data is integrated with  PowerBI for visualization. The dashboards and reports in PowerBI are configured to refresh daily, ensuring that they reflect the most up-to-date data.
