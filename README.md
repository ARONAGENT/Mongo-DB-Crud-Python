# MongoDB-CRUD-Project

## Overview
This project demonstrates how to perform CRUD (Create, Read, Update, Delete) operations on a MongoDB database using Python. The database is hosted on MongoDB Atlas, and we use the `pymongo` module for database connectivity. The project includes Jupyter Notebooks covering different MongoDB operations.

## Prerequisites
Before you begin, ensure you have the following installed:

- Python 3.x
- Jupyter Notebook
- `pymongo` module
- MongoDB Atlas account

## 1. Connecting to a MongoDB Cloud Database using `pymongo`
To connect to a MongoDB database on Atlas, follow these steps:

### Step 1: Install `pymongo`
```sh
pip install pymongo
```

### Step 2: Establish a Connection
Use the following Python script to connect to your MongoDB database:

```python
import pymongo

# Database connection details
client = pymongo.MongoClient("your-mongodb-atlas-connection-string")
db = client["your-database-name"]

print("Connected to MongoDB successfully!")
```

## 2. MongoDB Operations Covered in the Project
Each Jupyter Notebook covers a specific operation:

### 01. MongodbInsert.ipynb
- Inserts new records into the database.
```python
collection = db["your-collection-name"]
record = {"name": "John Doe", "age": 30, "city": "New York"}
collection.insert_one(record)
```

### 02. MongodbRetrieval.ipynb
- Fetches data from the database.
```python
records = collection.find()
for record in records:
    print(record)
```

### 03. MongodbUpdate.ipynb
- Updates existing records.
```python
query = {"name": "John Doe"}
new_values = {"$set": {"age": 35}}
collection.update_one(query, new_values)
```

### 04. MongodbDelete.ipynb
- Deletes records from the database.
```python
query = {"name": "John Doe"}
collection.delete_one(query)
```

## 3. Clone and Run the Project
### Step 1: Clone the Repository
```sh
git clone https://github.com/ARONAGENT/Mongo-DB-Crud-Python.git
cd MongoDB-CRUD-Project
```

### Step 2: Install Dependencies
```sh
pip install pymongo
```

### Step 3: Run Jupyter Notebook
```sh
jupyter notebook
```
Open the required notebook and follow the instructions inside.

## Conclusion
This project serves as a guide to using MongoDB with Python for common database operations. Feel free to modify and expand on it to suit your needs!

