# Banking Customer and Transaction Management System

**Technologies:** Python | MongoDB | PyMongo | Jupyter Notebook

## 📌 Project Overview

The Banking Customer and Transaction Management System is a beginner-friendly database project developed using Python and MongoDB. It demonstrates how banking customer information, account details, and transaction records can be stored, managed, and analyzed using a NoSQL database.

The project implements basic banking operations such as customer management, account balance updates, deposits, withdrawals, transaction history tracking, and banking data analysis.

> **Note:** This is an educational simulation using dummy data, not a production banking application.

## 🎯 Project Objectives

- Store and manage customer information using MongoDB.
- Maintain bank account details and balances.
- Perform CRUD operations using Python and PyMongo.
- Implement deposit and withdrawal functions.
- Validate transaction amounts and available account balances.
- Maintain transaction history.
- Analyze account balances and transaction activity using MongoDB aggregation.

## 🛠️ Technologies Used

- **Python:** Application logic and data processing.
- **MongoDB:** NoSQL database for storing banking records.
- **PyMongo:** Python driver for MongoDB connectivity and database operations.
- **Jupyter Notebook:** Interactive development and testing environment.
- **MongoDB Compass:** Optional graphical interface for exploring database documents.

## 📂 Database Structure

Database name: `banking_db`

### 1. Customers Collection

Stores customer information.

Example document:

```json
{
  "customer_id": "C101",
  "name": "Aarav Sharma",
  "city": "Pune",
  "age": 25
}
```

### 2. Accounts Collection

Stores bank account information.

```json
{
  "account_no": "ACC1001",
  "customer_id": "C101",
  "account_type": "Savings",
  "balance": 15000.0,
  "status": "Active"
}
```

### 3. Transactions Collection

Stores transaction history.

```json
{
  "account_no": "ACC1001",
  "transaction_type": "Deposit",
  "amount": 2000.0,
  "status": "Success"
}
```

Transaction records also include a transaction date.

## ⚙️ Features

### Customer Management
- Insert customer records.
- Search customers by ID or city.
- Update customer information.
- Delete dummy customer records for CRUD practice.

### Account Management
- Store account numbers and account types.
- View account balances.
- Filter accounts based on balance.
- Check whether an account is active.

### Transaction Management
- Deposit money into an active account.
- Withdraw money when sufficient balance is available.
- Validate positive transaction amounts.
- Record successful transactions.
- View transaction history.

### Banking Data Analysis
- Calculate total balances across accounts.
- Summarize deposits and withdrawals.
- Count transactions by type.
- Use MongoDB aggregation pipelines.

## 🚀 Installation and Setup

### Step 1: Install Python

Download Python from https://www.python.org/downloads/

### Step 2: Install MongoDB

Install MongoDB Community Server from:

https://www.mongodb.com/try/download/community

MongoDB Compass is optional.

### Step 3: Install PyMongo

Run the following command in your terminal or a Jupyter Notebook cell:

```bash
python -m pip install pymongo
```

In Jupyter Notebook, you can also use:

```python
%pip install pymongo
```

### Step 4: Start MongoDB

Make sure your local MongoDB Server is running.

### Step 5: Connect Python to MongoDB

```python
from pymongo import MongoClient

client = MongoClient(
    "mongodb://localhost:27017/",
    serverSelectionTimeoutMS=5000
)

client.admin.command("ping")

db = client["banking_db"]

customers = db["customers"]
accounts = db["accounts"]
transactions = db["transactions"]

print("MongoDB connected successfully!")
```

### Step 6: Execute the Project

Run the notebook cells in this order:

1. Import required libraries.
2. Connect to MongoDB.
3. Create database collections.
4. Insert sample customers and accounts.
5. Perform CRUD operations.
6. Implement deposit and withdrawal functions.
7. View transaction history.
8. Execute aggregation queries.
9. Verify the results in MongoDB Compass.

## 📊 Expected Learning Outcomes

- Understanding NoSQL database concepts.
- Connecting Python applications to MongoDB.
- Performing CRUD operations with PyMongo.
- Using MongoDB query operators such as `$gt`, `$gte`, `$set`, and `$inc`.
- Working with MongoDB aggregation stages such as `$match` and `$group`.
- Applying basic validation to banking transactions.
- Organizing structured application data into separate collections.

## 🔐 Limitations and Future Improvements

- Use MongoDB transactions for atomic balance updates and transaction logging.
- Add authentication and role-based access control.
- Implement unique account constraints and stronger validation.
- Use decimal-safe monetary representations rather than floating-point balances.
- Add a command-line interface or web interface.
- Implement automated tests and structured logging.
- Add secure audit trails and error handling.

## 👩‍💻 Author

**Tanvi Shire**

BCA Graduate | Python | SQL | MongoDB | Data Analytics

GitHub: https://github.com/tanvishire-dev

LinkedIn:https://www.linkedin.com/in/tanvi-s-b0b74a244/

## 📄 Disclaimer

This project is intended for educational and portfolio purposes only. All customer records are dummy data. It is not intended for real financial transactions or production banking use.
