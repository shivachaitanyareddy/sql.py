# sql.py
import sqlite3

conn = sqlite3.connect("test.db")
cursor = conn.cursor()

username = input("Enter username: ")

# Unsafe query construction
query = "SELECT * FROM users WHERE username = '" + username + "'"

cursor.execute(query)

print(cursor.fetchall())
