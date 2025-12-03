# Webscraping-and-Pandas
Web scraper that extracts the largest U.S. companies by revenue from Wikipedia and saves the data to a CSV file using Python, BeautifulSoup, and pandas.

# Largest U.S. Companies WebScraper

This Python project scrapes the list of the largest companies in the United States by revenue from Wikipedia and exports the data into a CSV file for analysis or further processing.

## Features
- Extracts the main data table of U.S. companies by revenue.
- Converts table headers and rows into a structured pandas DataFrame.
- Exports the resulting dataset as a CSV file.
- Handles potential HTTP restrictions by including a user-agent header.

## Technologies Used
- **Python 3**
- **BeautifulSoup** – for parsing HTML
- **requests** – for sending HTTP requests
- **pandas** – for creating and exporting DataFrames

## How It Works
1. The script sends a request to the Wikipedia page using `requests` with a browser-like User-Agent header.
2. `BeautifulSoup` parses the HTML page.
3. The code identifies the main table (`wikitable`) and extracts:
   - Column headers (`<th>` elements)
   - All table rows (`<tr>` elements)
4. Each row’s data is cleaned and added to a pandas DataFrame.
5. The DataFrame is exported to a CSV file for further use.
