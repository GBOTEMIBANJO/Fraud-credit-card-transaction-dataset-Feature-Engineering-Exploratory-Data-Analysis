# Fraud-credit-card-transaction-dataset-Feature-Engineering-Exploratory-Data-Analysis
This project involves exploring and analyzing a credit card transaction dataset with a focus on identifying fraudulent transactions using Feature Engineering and Exploratory Data Analysis (EDA) techniques.

Overview
In this project, we use a publicly available credit card transaction dataset and apply various feature engineering techniques to prepare the data for machine learning modeling. We then perform EDA to gain insights into the patterns and relationships in the data, especially focusing on identifying potential fraud-related trends.

This is the second part of a multi-part series on fraud detection, with the following sections:

Part 1: A gentle introduction to outlier detection
Part 2: Fraud credit card transaction dataset: Feature Engineering & EDA
Part 3: Fraud detection for credit card transactions: Modeling and Evaluation
Part 4: Model deployment with Docker and AWS
Dataset
The dataset contains information on credit card transactions, including:

Transaction time
Merchant information
Transaction amount
Location details
Customer details (gender, age, location, etc.)
Fraud label (0 for non-fraud, 1 for fraud)
The dataset is highly imbalanced, with a very small percentage of fraudulent transactions.

Project Structure
The source code structure of this project is organized as follows:

plaintext
Copy
├── datasets
│   ├── fraudTrain.csv
│   ├── fraudTest.csv
├── figs
│   ├── Fraud_count_vs_Age_vs_Category.png
│   ├── *.png
├── eda-feature-engineering.ipynb
├── eda-visualization.ipynb
├── LICENSE
├── .gitignore
├── requirements.txt
└── README.md
Key Files:
eda-feature-engineering.ipynb: Contains statistical summaries and feature engineering techniques.
eda-visualization.ipynb: Shows multiple visualization techniques for EDA tasks.
fraudTrain.csv and fraudTest.csv: The raw datasets containing credit card transactions.
figs/: Contains visualizations of the EDA process saved as PNG files.
requirements.txt: Lists the Python dependencies required to run the code.
Feature Engineering
Feature engineering techniques were applied to the dataset to extract meaningful features and improve the performance of machine learning models. Some of the key steps included:

Datetime Conversion: transaction_time and birthday were converted to datetime format to extract additional features like the transaction year, month, day, and hour.
Age Calculation: Age was calculated from the birthday feature.
Distance Calculation: Longitude and latitude values for both the client and merchant were used to calculate the distance between the client and the merchant.
Binning Age: Age was categorized into different intervals such as 'Less than 20', 'Between 20 and 30', 'Between 30 and 40', etc.
Gender Conversion: 'M' and 'F' were mapped to 'Male' and 'Female' respectively.
Exploratory Data Analysis (EDA)
EDA was performed using visualizations and statistical summaries to uncover insights in the data. Key findings include:

Age Distribution: The distribution of fraud transactions is impacted by age, with older age groups being more likely to experience fraud.
Transaction Amount: The average fraud transaction amount was compared to normal transactions, revealing a higher median amount for fraud cases.
Time-based Patterns: Fraudulent transactions show higher occurrences in specific months and times of the day.
Key Visualizations
Fraud Transaction Amount per Age Group: A box plot was used to show the distribution of fraud transaction amounts across different age groups.
Fraud by Gender: A comparison of fraud transactions based on gender was visualized.
Fraud per Category: A breakdown of fraud cases across different transaction categories (e.g., grocery, shopping, gas) was explored.
Fraud Transactions by Time: Time-based trends were visualized to identify when fraud is most likely to occur.
Requirements
To run the code in this repository, you will need the following Python libraries:

pandas
numpy
seaborn
matplotlib
You can install the necessary dependencies using the following command:

bash
Copy
pip install -r requirements.txt
Conclusion
This project demonstrates the importance of Feature Engineering and Exploratory Data Analysis (EDA) in understanding and preparing a dataset for machine learning. By creating meaningful features and visualizing key insights, we can better understand the patterns associated with fraudulent transactions, which will aid in the subsequent modeling process.

How to Run
Clone the repository.
Download the fraudTrain.csv and fraudTest.csv datasets from the provided link and add them to the datasets/ folder.
Install the required dependencies using pip install -r requirements.txt.
Run the Jupyter notebooks (eda-feature-engineering.ipynb and eda-visualization.ipynb) to explore and analyze the dataset.
