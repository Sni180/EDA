This project contains a Jupyter Notebook that performs Exploratory Data Analysis (EDA) on a dataset of FIFA player statistics. The analysis covers data ingestion, cleaning, feature engineering, and visualization of key player attributes and club performance.

🎯 Project Goal
The primary goal of this notebook is to understand the structure and quality of the FIFA player data and to extract meaningful insights through statistical summaries and visualizations.

✨ Features
The Creating Graphs.ipynb notebook performs the following key tasks:

Data Ingestion: Securely fetches the fifa_eda.csv dataset directly from an anonymous public AWS S3 bucket (s3://eda-python) using boto3.

Data Cleaning & Inspection:

Checks for and reports the count of missing values in each column.

Verifies the dataset for duplicate rows (none found).

Feature Engineering: Calculates a new feature, Years_Joined, which estimates the tenure of the player at their current club.

Data Visualization:

Displays the Age Distribution of players using a histogram.

Creates a bar chart showing the Top 5 Clubs with the highest average Potential rating.

🛠️ Prerequisites
To run this notebook locally, you need a Python environment with the following libraries installed:

pandas: For data manipulation and analysis.

boto3: The AWS SDK for Python, used to connect to and fetch data from S3.

botocore: A low-level interface to AWS services (used here for anonymous S3 access).

matplotlib: For creating visualizations (histograms and bar charts).

You can install the required packages using pip:

Bash

pip install pandas boto3 matplotlib
🚀 Usage
Clone the Repository (if applicable):

Bash

git clone <repository-url>
cd <repository-name>
Open the Notebook: Launch Jupyter Notebook or JupyterLab and open the file:

Bash

jupyter notebook "Creating Graphs.ipynb"
Run the Cells: Execute the cells sequentially. The code will automatically connect to S3, download the data, and perform the analysis and visualization steps.

📁 Data Source
The analysis uses the fifa_eda.csv file, which is retrieved programmatically from the following AWS S3 location:

Bucket: eda-python

Key: fifa_eda.csv

The S3 connection is configured to be anonymous (Config(signature_version=UNSIGNED)), allowing direct access to the public data.
