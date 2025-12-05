# Lecture 17

---

## API

- Application Programming Interface
- Data pipelines that share data between applications
- Commonly used to fetch data from web services
- Returns data in a structured format (JSON, XML)
- Format: json
  {
  "name": "John",
  "age": 30,
  "city": "New York"
  }
- JSON Viewer: https://jsonviewer.stack.hu/
- Example:

  ```python
  import requests

  response = requests.get('https://api.example.com/data')
  data = response.json()
  ```

- Upload datasets to kaggle: https://www.kaggle.com/datasets
