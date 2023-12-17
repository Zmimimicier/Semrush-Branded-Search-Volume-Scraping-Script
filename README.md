# Automated Keyword Volume Scraping Tool

This Python script automates the process of scraping keyword volume data from the SEMrush platform. It supports a user-specified list of keywords, dates, and databases, leveraging Selenium for web scraping, Openpyxl for Excel manipulation, and Pandas for data processing.

## Features:

### User Input:

- The script prompts the user to input a list of keywords, select a target database (e.g., "us," "uk"), and provide a list of dates.

### Excel Workbook Creation:

- Generates an Excel workbook with two sheets: one for the specified database's volume and another for the global volume.

### Web Scraping:

- Utilizes Selenium WebDriver to log in to the SEMrush platform (credentials required) and scrape keyword volume data for each keyword and date.

### Data Validation and Handling:

- Handles potential errors such as NoSuchElementException during web scraping and retries the process up to three times before moving on.

### Data Transformation:

- Defines a function (`value_to_float`) to convert scraped volume data into numeric format, handling cases like 'K' for thousands, 'M' for millions, and 'B' for billions.

### Excel File Modification:

- Processes the scraped data, transforms it using the defined function, and saves the modified DataFrames into a new Excel file (`output_modified.xlsx`).

### Output:

- The final output includes two Excel files: one with raw scraped data (`output.xlsx`) and another with transformed and cleaned data (`output_modified.xlsx`).

## Usage:

### Prerequisites:

- Ensure you have the required Python packages installed (`pandas`, `openpyxl`, `selenium`), and download the appropriate Selenium WebDriver for Chrome.

### Credentials:

- Provide your SEMrush login credentials in the script.

### Execution:

- Run the script, input the necessary information, and follow the instructions. Make sure to log in manually when prompted.

### Output:

- Retrieve the final output Excel files for analysis.

## Note:

- This script assumes the availability and accessibility of the SEMrush platform, and any changes to the platform structure may affect its functionality.
