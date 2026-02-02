# Python Scripting for Databases

Python provides robust support for interacting with databases, enabling developers to connect, query, and manage data efficiently. Below are the steps to work with popular databases like SQLite, MySQL, and PostgreSQL using Python.

# 1. SQLite

SQLite is a lightweight, serverless database that comes pre-installed with Python.

Steps:

1: Import the sqlite3 module.

2: Establish a connection to the database (creates a new file if it doesn’t exist).

3: Use a cursor object to execute SQL queries.

Example:

import sqlite3

# Connect to SQLite database
connection = sqlite3.connect("example.db")
cursor = connection.cursor()

# Create a table
cursor.execute("""
CREATE TABLE IF NOT EXISTS users (
id INTEGER PRIMARY KEY AUTOINCREMENT,
name TEXT NOT NULL,
age INTEGER
)
""")

# Insert data
cursor.execute("INSERT INTO users (name, age) VALUES ('Alice', 30)")
connection.commit()

# Fetch data
cursor.execute("SELECT * FROM users")
print(cursor.fetchall())

connection.close()

# 2. MySQL

For MySQL, you need the mysql-connector-python library.

Steps:

1: Install the library:

pip install mysql-connector-python

2: Connect to the MySQL server.

3: Execute queries using a cursor.

Example:

import mysql.connector

# Connect to MySQL database
connection = mysql.connector.connect(
host="localhost",
user="root",
password="password",
database="test_db"
)
cursor = connection.cursor()

# Create a table
cursor.execute("""
CREATE TABLE IF NOT EXISTS users (
id INT AUTO_INCREMENT PRIMARY KEY,
name VARCHAR(100),
age INT
)
""")

# Insert data
cursor.execute("INSERT INTO users (name, age) VALUES ('Bob', 25)")
connection.commit()

# Fetch data
cursor.execute("SELECT * FROM users")
print(cursor.fetchall())

connection.close()

# 3. PostgreSQL

For PostgreSQL, use the psycopg2 library.

Steps:

1: Install the library:

pip install psycopg2

2: Connect to the PostgreSQL server.

3: Use a cursor to execute SQL commands.

Example:

import psycopg2

# Connect to PostgreSQL database
connection = psycopg2.connect(
dbname="test_db",
user="postgres",
password="password",
host="localhost"
)
cursor = connection.cursor()

# Create a table
cursor.execute("""
CREATE TABLE IF NOT EXISTS users (
id SERIAL PRIMARY KEY,
name TEXT NOT NULL,
age INTEGER
)
""")

# Insert data
cursor.execute("INSERT INTO users (name, age) VALUES ('Charlie', 35)")
connection.commit()

# Fetch data
cursor.execute("SELECT * FROM users")
print(cursor.fetchall())

connection.close()
