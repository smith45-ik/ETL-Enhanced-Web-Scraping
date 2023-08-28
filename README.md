# Enhanced ETL Web Scraping with BeautifulSoup

Welcome to the Enhanced ETL Web Scraping GitHub repository! This project focuses on utilizing the power of Python along with
the BeautifulSoup, Requests, and Pandas libraries to perform Extract, Transform, and Load (ETL) processes on various web sources.
In this repository, you'll find the code and resources used to scrape data from different websites, transform it into a usable format,
and load it into CSV files for easy accessibility and analysis.

# Tools Used and How They are Used

- Python: The programming language that forms the foundation of this project, allowing us to write the scripts for web scraping, data manipulation, and transformation.

- BeautifulSoup: A powerful library in Python for web scraping purposes. It assists in pulling data from HTML and XML files, making it easier to extract the relevant information from web pages.

- Requests: This library is used to send HTTP requests to web pages and receive responses, which are then used in conjunction with BeautifulSoup for data extraction.

- Pandas: A versatile data manipulation library that aids in cleaning, transforming, and structuring the scraped data. It provides tools to efficiently work with tabular data.

# Data and Sources

In this repository, we've performed ETL-enhanced web scraping on three different websites to gather insightful data:

1. List of largest companies in the United States by revenue from Wikipedia: We've extracted, transformed, and loaded data related to the top US companies by revenue. The scraped data includes company names, industries, and revenue figures.

2. Economy of Nigeria from Wikipedia: Our ETL process here involved scraping and structuring economic data about Nigeria. We collected information about various economic indicators, sectors, and growth statistics.

3. books.toscrape.com/catalogue: From this website, we've scraped details about different books, including titles, prices, availability, and book cover images.

# Extracting data using BeautifulSoup and Requests:

```
import requests
from bs4 import BeautifulSoup

# Send a GET request to the website
response = requests.get(url)

# Parse the HTML content using BeautifulSoup
soup = BeautifulSoup(response.content, 'html.parser')

# Find and extract specific elements
data = soup.find_all('div', class_='data-element')
```

# Transforming data using Pandas:

```
import pandas as pd

# Create a DataFrame from the extracted data
df = pd.DataFrame(data, columns=['Name', 'Value'])

# Perform data cleaning and transformation
df['Value'] = df['Value'].apply(clean_value)
df['Name'] = df['Name'].str.strip()
```

# Loading data into a CSV file:

```
# Save the DataFrame to a CSV file
df.to_csv('output_data.csv', index=False)
```

# Outcome of the Project

The outcome of this project demonstrates how to effectively leverage web scraping techniques to gather valuable data from diverse sources, transform it into a structured format, and save it for future analysis. By following the provided code snippets and explanations, you'll learn how to:

- Use BeautifulSoup and Requests to extract data from web pages.
- Employ Pandas to transform and clean the scraped data.
- Organize the data into CSV files for easy sharing and analysis.
- Apply ETL principles to web scraping, making the data more meaningful and accessible.

# Conclusion

This repository serves as an educational resource and a practical guide to using web scraping for ETL purposes. By exploring the code snippets and understanding the methodologies applied, you'll gain valuable insights into collecting, structuring, and utilizing data from different websites. Whether you're interested in business analytics, economic insights, or book cataloging, the techniques presented here are versatile and can be adapted for a wide range of applications.

Feel free to explore the code, experiment with the techniques, and adapt them to your specific needs. Happy web scraping!

