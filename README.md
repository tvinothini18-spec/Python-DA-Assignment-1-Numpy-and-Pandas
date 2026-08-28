Assignment 3 – NumPy and Pandas Fundamentals
📌 Project Overview
This project is part of my Data Science learning journey and focuses on the fundamentals of NumPy and Pandas using Python.
The project demonstrates practical operations on numerical arrays, Pandas Series, and tabular transaction data. It covers array creation and manipulation, indexing and slicing, data exploration, filtering, aggregation, and DataFrame modification.
🎯 Objectives
The objectives of this project are to:
Create and work with NumPy arrays.
Understand NumPy array properties such as shape, data type, and size.
Perform mathematical operations on NumPy arrays.
Convert Celsius temperatures to Fahrenheit.
Calculate minimum, maximum, and mean temperatures.
Perform array indexing and slicing.
Work with one-dimensional and two-dimensional arrays.
Create and manipulate Pandas Series.
Perform indexing, slicing, and filtering on Series.
Create and explore Pandas DataFrames.
Filter DataFrame records based on conditions.
Perform aggregation using groupby().
Add, update, and remove DataFrame data.
🛠️ Technologies Used
Python
NumPy
Pandas
Jupyter Notebook
📂 Project Structure
Assignment3/
│
├── Assignment3.ipynb
└── README.md
🔢 Part 1 – NumPy Array Operations
The first part of the project focuses on working with temperature data using NumPy.
1. Creating a 1D NumPy Array
A one-dimensional array containing temperature values for one week is created.
temperatures_w1 = np.array([
    22.5, 25.3, 20.8, 23.4,
    26.1, 24.8, 21.9
])
2. Inspecting Array Properties
The following NumPy properties are explored:
shape
dtype
size
3. Array Operations
The project performs:
Celsius to Fahrenheit conversion
Minimum temperature calculation
Maximum temperature calculation
Mean temperature calculation
The Fahrenheit conversion is performed using:
Fahrenheit = (Celsius × 9/5) + 32
4. Array Indexing and Slicing
The project extracts:
First three days of the week
Weekend temperatures
Middle three days of the week
Example:
first_three = temperatures_w1[:3]
weekend = temperatures_w1[-2:]
middle_three = temperatures_w1[2:5]
5. Two-Dimensional NumPy Array
Temperature data for two weeks is stored in a 2D NumPy array.
The project demonstrates:
Accessing Week 1 data
Accessing Week 2 data
Extracting weekend temperatures
Checking array shape
Checking data type
Checking array size
🐼 Part 2 – Pandas Series
The second part introduces Pandas Series using student marks.
Creating a Series
marks = pd.Series(
    [95, 92, 89, 85, 80],
    index=['Rank1', 'Rank2', 'Rank3', 'Rank4', 'Rank5']
)
Series Operations
The following operations are performed:
Create a Pandas Series
Access values using positional indexing
Select the top three ranks
Access the third rank
Filter marks greater than 90
Update the marks of Rank 1
Remove Rank 5
Calculate CGPA
The project uses both:
marks.iloc[0]
and:
marks.loc['Rank1']
to demonstrate positional and label-based indexing.
📊 Part 3 – Pandas DataFrame
The third part focuses on transaction data using a Pandas DataFrame.
The DataFrame contains the following columns:
Column
Description
TransactionID
Unique transaction identifier
ProductCategory
Category of the product
Region
Region of the transaction
Amount
Transaction amount
The dataset contains transaction records across Electronics, Clothing, and Furniture categories and different regions.
🔍 Data Exploration
The following DataFrame exploration operations are performed:
Display the complete DataFrame
Display the first five rows
Display the last five rows
Check DataFrame shape
Display column names
Check data types
Select ProductCategory and Amount
Select the last three columns
Filter transactions from the North region with amount greater than 200
Count occurrences of each product category
Find unique regions
Calculate mean transaction amount by region
Example Filtering
filtered_data = transactions[
    (transactions['Region'] == 'North') &
    (transactions['Amount'] > 200)
]
Product Category Counts
transactions['ProductCategory'].value_counts()
Mean Amount by Region
transactions.groupby('Region')['Amount'].mean()
✏️ DataFrame Manipulation
The project also demonstrates modifying the transaction DataFrame.
Update Transaction Amount
The amount for TransactionID 102 is updated to 165.
transactions.loc[
    transactions['TransactionID'] == 102,
    'Amount'
] = 165
Add a Discount Column
A new Discount column is created using 10% of the transaction amount.
transactions['Discount'] = transactions['Amount'] * 0.10
Remove a Transaction
The transaction with TransactionID 109 is removed.
transactions = transactions[
    transactions['TransactionID'] != 109
]
Remove the Discount Column
The Discount column is deleted from the DataFrame.
transactions = transactions.drop('Discount', axis=1)
📚 Key Concepts Practiced
This project provided hands-on practice with:
NumPy
NumPy array creation
1D arrays
2D arrays
Array properties
Mathematical operations
min()
max()
mean()
Indexing
Slicing
Pandas Series
Series creation
.loc
.iloc
Boolean filtering
Updating values
Removing values
Basic calculations
Pandas DataFrame
DataFrame creation
head()
tail()
shape
columns
dtypes
Column selection
Conditional filtering
value_counts()
unique()
groupby()
Updating values
Adding columns
Removing rows
Removing columns
🚀 How to Run the Project
1. Install Python
Make sure Python is installed on your system.
2. Install Required Libraries
pip install numpy pandas jupyter
3. Open the Notebook
Run:
jupyter notebook
Then open:
Assignment3.ipynb
The notebook can also be opened using JupyterLab, VS Code, or Google Colab.
📈 Learning Outcome
Through this assignment, I gained practical experience in using NumPy and Pandas, which are essential libraries for Data Science and Data Analysis.
This project strengthened my understanding of:
Numerical data manipulation
Array operations
Data indexing and slicing
Tabular data handling
Data filtering
Data aggregation
Basic data transformation
These concepts provide a foundation for progressing toward Data Cleaning, Exploratory Data Analysis (EDA), Data Visualization, Statistics, and Machine Learning.
