# Credit Card Churning prediction:
This project aims to detect customers who are possibly planning to close their credit card account.

This project uses Databricks to run the project on Spark and uses Azure Data Factory for the pipeline execution.

### Pipeline:
![image](https://github.com/user-attachments/assets/6df8f2fa-ebc6-4e4b-9b44-2460279acb99)

1. The copy dataset activity copies the data from the Github repository and stores it in Azure ADLS.
2. The Databricks EDA Activity performs EDA on the data stored in Azure.
3. The Credit Card Transformation activity transforms the data such as performing String Indexing, One Hot Encoding, Vector Assembling, Scaling and SMOTE. The test and train data are stored back in ADLS as parquet files.
4. The Machine Learning activity runs ML model on the test data by training on the train data. A report is generated on the model metrics.


