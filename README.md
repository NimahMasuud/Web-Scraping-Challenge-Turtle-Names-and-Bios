# Web Scraping Challenge: Turtle Names and Bios

## Description
This repository contains the solution for the web scraping challenge. The task involves extracting turtle names and their bios from the website:[Scrape This Site - Frames](https://www.scrapethissite.com/pages/frames/). 
The extracted data is saved in a CSV file.

## Challenge Details
- **Target Website:** [https://www.scrapethissite.com/pages/frames/](https://www.scrapethissite.com/pages/frames/)
- **Objective:** Extract the names of turtles and their bios.
- **Output Format:** CSV file containing the following columns:
  - `Turtle Name`
  - `Bio`

## Solution Overview
The solution is implemented using Python with the `BeautifulSoup` library from `bs4` for parsing HTML, and `requests` for handling HTTP requests. The scraped data is written into a CSV file using Python's built-in `csv` module.

## Usage

### Prerequisites
- Python 3.x
- Required libraries:
  - `requests`
  - `beautifulsoup4`

Install the required libraries by running:
```bash
pip install requests beautifulsoup4
```

### Steps to Run the Script
1. Clone this repository:
   ```bash
   git clone <repository-url>
   ```
2. Navigate to the project directory:
   ```bash
   cd web_scraping_challenge
   ```
3. Run the script:
   ```bash
   python scrape_turtles.py
   ```
4. Find the output CSV file (`turtles_data.csv`) in the project directory.

## File Structure
- `scrape_turtles.py`: Python script for scraping the data.
- `turtles_data.csv`: Generated CSV file containing the turtle names and bios.
- `README.md`: Documentation of the project.

## Approach
1. **Sending HTTP Requests:**
   - Use the `requests` library to send a GET request to the target URL.
2. **Parsing HTML Content:**
   - Use `BeautifulSoup` to parse the response and locate the iframe containing the data.
   - Extract the iframe URL and make a request to it.
3. **Extracting Data:**
   - Parse the HTML structure of the iframe page to locate turtle names and bios.
   - Use CSS selectors to extract specific elements.
4. **Saving Data:**
   - Save the extracted data into a CSV file.
