# Lecture 18

---

## Web Scraping

- Web scraping is the process of extracting data from websites.
- Commonly used to gather data from web pages that do not provide an API.
- Libraries for web scraping in Python:
  - BeautifulSoup
  - Scrapy
  - Selenium
- Important considerations:
  - Respect the website's `robots.txt` file.
  - Avoid overloading the server with too many requests.
  - Be aware of legal and ethical implications.
- Basic steps for web scraping:
  1. Send a request to the website's server to retrieve the HTML content.
  2. Parse the HTML content to locate the desired data.
  3. Extract and store the data in a structured format (e.g., CSV, JSON).
- Example using BeautifulSoup:
  ```python
  import pandas as pd
  import requests
  from bs4 import BeautifulSoup
  url = 'http://example.com'
  response = requests.get(url)
  soup = BeautifulSoup(response.text, 'html.parser')
  data = []
  for item in soup.find_all('tag'):  # Replace 'tag' with the actual HTML tag
      data.append(item.text)
  df = pd.DataFrame(data, columns=['Column Name'])  # Replace 'Column Name' with actual column name
  df.to_csv('output.csv', index=False)
  ```
- Always check the website's terms of service before scraping.
