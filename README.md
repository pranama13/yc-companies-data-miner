# yc-companies-data-miner
This project scrapes data from the [Y Combinator company directory](https://www.ycombinator.com/companies), including company names, batches, descriptions, and founder LinkedIn profiles.

Designed to run seamlessly in **Google Colab** using headless Chrome and Selenium.

---

## 🚀 Getting Started in Google Colab

### 🔧 1. Install Chrome, ChromeDriver, and Required Packages

!apt-get update
!apt install chromium-chromedriver
!cp /usr/lib/chromium-browser/chromedriver /usr/bin
!pip install selenium pandas requests beautifulsoup4
⚙️ 2. Set Up Selenium in Headless Mode

from selenium import webdriver
from selenium.webdriver.chrome.options import Options

chrome_options = Options()
chrome_options.add_argument('--headless')
chrome_options.add_argument('--no-sandbox')
chrome_options.add_argument('--disable-dev-shm-usage')

driver = webdriver.Chrome('chromedriver', options=chrome_options)

📥 3. Copy and Run the Scraper Code
Paste your scraping logic after the setup (you can split it into cells or import it from a .py file on GitHub or Google Drive).

📦 Output
A file named CompaniesDetails.csv saved to your Colab environment

You can download it by running:


from google.colab import files
files.download("CompaniesDetails.csv")
📋 Features
Headless Chrome browsing with Selenium

Scrolling to load full list of Y Combinator companies

Scrapes:

Company Name

YC Batch

Short Description

Founder Names

LinkedIn URLs

Outputs a clean CSV file

📝 Notes
Don't forget to wait for page elements to load (via time.sleep or WebDriverWait)

Keep a reasonable delay between requests to avoid hitting server limits

This code assumes the Y Combinator site structure remains stable
