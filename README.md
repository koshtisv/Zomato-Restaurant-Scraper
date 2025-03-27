# Zomato Restaurant Scraper

This project is a Python-based web scraper that extracts restaurant details from Zomato using Selenium and BeautifulSoup.

## Features
- Extracts restaurant names, links, cuisines, prices, addresses, ratings, and contact details.
- Navigates to each restaurant's detail page and extracts information.
- Saves the extracted data into a CSV file (`mydata.csv`).
- Uses Selenium for automated browsing and data collection.

## Prerequisites
Ensure you have the following installed:
- Python 3.x
- Google Chrome
- Chrome WebDriver
- Required Python libraries:
  ```bash
  pip install selenium beautifulsoup4 pandas requests
  ```

## Project Structure
```
Zomato-Hotel-Scraper/
│── main.py          # Main script to scrape restaurant details
│── mydata.csv       # Extracted restaurant data (generated after running the script)
│── README.md        # Project documentation
```

## Usage
1. **Run the script**:
   ```bash
   python main.py
   ```
2. The script will:
   - Open Zomato's restaurant listing for a given location (e.g., `chinchwad` in Pune).
   - Scroll down to load more restaurants.
   - Click each restaurant, extract details, and return to the main page.
   - Save data to `mydata.csv`.

## Potential Issues & Fixes
- **Class name changes**: Zomato frequently updates its website structure. If the script fails to find elements, update the class names in `main.py`.
- **WebDriver issues**: Ensure ChromeDriver is compatible with your Chrome version.
- **Timeout errors**: Increase `time.sleep()` durations if pages take longer to load.

## License
This project is licensed under the MIT License.
