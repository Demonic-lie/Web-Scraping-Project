# Web Scraping Project Documentation

## Overview
This web scraping project aims to extract job postings and related information from SimplyHired.com. The scope includes scraping job titles, company names, locations, job descriptions, salaries, quick apply options, and date stamps.

## Project Structure
The project consists of Python scripts for web scraping, data cleaning, and analysis. The main files include `SimplyHired_Scraper.ipynb`. Additionally, there are utility modules for handling HTTP requests, parsing HTML content, and managing scraped data.


## Libraries or Tools used.

1. Beautiful Soup (bs4): A Python library for pulling data out of HTML and XML files. It provides simple ways to navigate, search, and modify the parse tree.

2. requests: A popular HTTP library for making requests in Python. It allows you to send HTTP requests easily.

3. headers_random: This is a custom module for generating random HTTP headers. It's used to mimic different user agents and headers to avoid being blocked by websites during scraping.

4. cloudscraper: A Python module for bypassing Cloudflare's anti-bot page (CAPTCHA) and scraping the content protected by Cloudflare.

5. datetime: A module for working with dates and times in Python. It's used for managing timestamps.

6. csv: A module for reading and writing CSV files. It's used to store scraped data in a structured format.

7. os: A module for interacting with the operating system. It's used for tasks like reading environment variables, manipulating file paths, etc.


## Installations:

pip install beautifulsoup4
pip install requests
pip install cloudscraper


## Instructions on how to run script.

### Prerequisites

Before running the script, ensure you have Python installed on your system. You can download Python from the official website: [Python.org](https://www.python.org/).

Installation

1. Clone the directory to your local machine or download the script files directly.

2. Navigate to the directory where the script files are located.

3. Install the required Python libraries 

### Usage

1. Open the notebook file (`SimplyHired_Scraper.ipynb`) using Jupyter Notebook, JupyterLab, or any compatible environment.

2. Replace the `url` variable in the notebook with the URL you want to scrape data from. Ensure it's the correct URL from SimplyHired.

3. Run each cell of the notebook sequentially. Here's a breakdown of what each cell does:
   - Cell 1: Imports necessary libraries and modules.
   - Cell 4: Sends a request to the specified URL and checks if the response status code is 200 (OK). If not, rerun the cell until a 200 status code is obtained.
   - Other Cells: Contains code for scraping data, parsing HTML content, and storing data. Run them as needed.

4. Ensure that each cell runs successfully and without errors. If errors occur, check for any missing dependencies and rerun

5. Once all cells have been executed successfully, you should have the scraped data available in csv file Jobs_Postings.csv


### Notes
- It may take multiple attempts to obtain a response status code of 200 from the URL. If the status code is not 200, rerun the cell that sends the request until the desired status code is obtained.
- Make sure to comply with the terms of service and usage policies of SimplyHired or any other website being scraped. Avoid sending too many requests in a short period to prevent IP bans or other restrictions.



## Assumptions made:

1. Uniform HTML Structure: It is assumed that all sub-sites of the SimplyHired website follow the same naming pattern and have a consistent HTML structure. Any variations in the structure might affect the scraping process and require adjustments to the code.

2. Consistent Data Retrieval: The script assumes that the data retrieval process remains consistent across different pages of the SimplyHired website. Any changes in the structure or content layout may require modifications to the scraping logic.

3. Stable Response Codes: The script relies on receiving a response status code of 200 (OK) from the server. It's assumed that eventual success is achievable by rerunning the cell responsible for sending the request until the desired status code is obtained.

4. No Dynamic Content: It's assumed that the content being scraped is static and does not rely heavily on client-side rendering or dynamic updates. If the website heavily utilizes JavaScript or AJAX to load content dynamically, additional handling may be necessary.




## Data Sources
The primary data source for this project is SimplyHired.com, a job search engine website. The scraping process targets specific search result pages containing job listings in various categories and locations.

## Scraping Process
The scraping process involves sending HTTP requests to SimplyHired.com, parsing the HTML content using BeautifulSoup, and extracting relevant job information such as titles, company names, locations, descriptions, salaries, quick apply options, and date stamps. The process adheres to the directives specified in the `robots.txt` file to ensure compliance with the website's terms of service.

## Data Cleaning
After scraping the job postings, the data is cleaned and preprocessed to remove any inconsistencies or irrelevant information. This includes handling missing values, standardizing data formats, and filtering out duplicate entries.

## Legal and Ethical Considerations
The web scraping project respects the directives specified in the `robots.txt` file of SimplyHired.com to ensure compliance with the website's terms of service. The scraping process is conducted responsibly, with appropriate rate limiting and throttling mechanisms in place to avoid overloading the website's servers. Additionally, data privacy and security are prioritized, and no sensitive information is used.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Author
- [Anjali Kumari](https://github.com/Demonic-lie)

## Acknowledgements
Special thanks to SimplyHired.com for providing access to their job listing data for educational purposes.

## Contact
For questions, feedback, or collaboration opportunities, please contact [https://www.linkedin.com/in/anjalikumari999/]).

