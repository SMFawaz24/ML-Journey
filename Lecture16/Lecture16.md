# Lecture 16

---

## JSON Files

- JavaScript Object Notation
- Universal Format
- API gives data in JSON format
- Easily parsed in Python using `json` module
- Example:

  ```python
  import json

  with open('data.json') as f:
      data = json.load(f)
  ```

## SQL

- Structured Query Language
- Load data directly from databases using Pandas
- Use SQL queries to filter data before loading
- Example:

  ```python
  import pandas as pd
  import sqlite3

  conn = sqlite3.connect('database.db')
  df = pd.read_sql_query("SELECT * FROM table_name", conn)
  ```
