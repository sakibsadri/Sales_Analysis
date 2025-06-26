🪔 Diwali Sales Analysis - Python Project
This project involves cleaning, analyzing, and visualizing sales data for Diwali shopping using Python. The goal is to derive meaningful business insights from customer purchase behavior.

📁 Dataset
File Name: Diwali Sales Data.csv

Rows: 11251

Columns: 15 (later cleaned to 13)

Source: Sample dataset for retail analytics

📊 Tools & Libraries Used
Python

Pandas

NumPy

Seaborn

Matplotlib

🔧 Steps Performed
Imported Libraries
numpy, pandas, matplotlib.pyplot, seaborn

Loaded Dataset

python
Copy
Edit
df = pd.read_csv('Diwali Sales Data.csv', encoding='unicode_escape')
Initial Data Exploration

Used .shape, .head(), .info(), .describe() to understand data

Checked and removed null values

Dropped irrelevant columns like 'Status' and 'unnamed1'

Data Cleaning

Converted Amount column from float64 to int64

Removed rows with missing values using dropna()

Data Analysis

Used groupby() and aggregation to analyze sales trends

Performed gender-based and age-group-based comparisons

Visualization

Count plots for Gender and Age Group

Bar plots for Total Sales by Age Group

📈 Insights
Age group 26-35 has the highest total purchase amount.

Males tend to spend more than females in this dataset.

Government and IT sector customers are among the highest spenders.

📌 Sample Visuals
Gender Distribution

python
Copy
Edit
sns.countplot(x='Gender', data=df)
Age Group vs Sales

python
Copy
Edit
sales_age = df.groupby(['Age Group'], as_index=False)['Amount'].sum()
sns.barplot(x='Age Group', y='Amount', data=sales_age)
📁 Folder Structure
Copy
Edit
Diwali-Sales-Analysis/
│
├── Diwali Sales Data.csv
├── analysis.ipynb
└── README.md
✅ Future Improvements
Add time-series analysis if timestamps are available

Build interactive dashboards using Power BI or Plotly Dash

Include customer segmentation using clustering

📬 Contact
If you have any questions or suggestions, feel free to reach out!
