# 🕸️ Job Listing Scraper

A Python-based web scraping project built using **BeautifulSoup** and **Requests**, designed to extract job-like listings from a web source and save them into a structured CSV file.

---

## 📋 Project Overview

This project demonstrates the fundamentals of web scraping using Python. It scrapes listing data (title, author/company, location) across multiple pages of a target website and exports the results to a CSV file for further analysis.

> **Source Website:** [quotes.toscrape.com](http://quotes.toscrape.com) — used as a structured scraping practice site to simulate job listing extraction.

---

## 📁 Project Files

| File | Description |
|------|-------------|
| `Job_Listing_Scraper.ipynb` | Jupyter Notebook with full scraping code and output |
| `job_listings.csv` | Output CSV file containing scraped listings |

---

## ⚙️ How It Works

The scraper is built step-by-step across the following notebook sections:

| Step | Description |
|------|-------------|
| 1 | **Import Libraries** — `requests`, `BeautifulSoup`, `time`, `csv` |
| 2 | **Set Up Scraper** — Define base URL and browser-mimicking headers |
| 3 | **Helper Function** — `get_soup()` sends HTTP request and returns parsed HTML |
| 4 | **Scrape Single Listing** — `scrape_job()` extracts Title, Company, and Location from one item |
| 5 | **Get Page Items** — `get_job_items()` finds all listing elements on a page |
| 6 | **Total Pages** — `get_total_pages()` sets the number of pages to scrape (5 pages) |
| 7 | **Scrape All Listings** — `scrape_all_jobs()` loops through all pages with a 1-second delay |
| 8 | **Display Output** — Prints all scraped listings to console |
| 9 | **Save to CSV** — `save_jobs_to_csv()` writes data to `job_listings.csv` |
| 10 | **Execute & Save** — Runs the full scraping pipeline |
| 11 | **Read CSV** — Reads and verifies the saved CSV file |

---

## 📦 Requirements

```
Python 3.x
requests
beautifulsoup4
```

Install dependencies with:

```bash
pip install requests beautifulsoup4
```

---

## 🚀 How to Run

1. Clone or download this repository.
2. Open `Job_Listing_Scraper.ipynb` in **Jupyter Notebook** or **VS Code**.
3. Run all cells in order (top to bottom).
4. The scraped data will be saved automatically to `job_listings.csv` in the same directory.

---

## 📄 Output Format

The CSV file contains the following columns:

| Column | Description |
|--------|-------------|
| `Job Title` | The listing title / quote text |
| `Company` | Author name (simulates company field) |
| `Location` | Set to `India` (simulated location field) |

**Sample Output:**

```
Job Title, Company, Location
"The world as we have created it...", Albert Einstein, India
"It is our choices Harry...", J.K. Rowling, India
...
```

Total records scraped: **20 listings** across 5 pages.

---

## 🛠️ Technologies Used

| Tool | Purpose |
|------|---------|
| Python 3 | Core programming language |
| `requests` | HTTP requests to fetch web pages |
| `BeautifulSoup4` | HTML parsing and data extraction |
| `csv` | Writing scraped data to CSV |
| `time` | Adding delay between requests |
| Jupyter Notebook | Interactive development environment |

---

## 🔍 Key Concepts Demonstrated

- Sending HTTP GET requests with custom headers to avoid blocking
- Parsing HTML using BeautifulSoup
- Navigating DOM elements by tag and class
- Multi-page scraping with pagination
- Polite scraping with `time.sleep()` delay
- Exporting structured data to CSV

---

## 👤 Author

**Tejas**
Web Scraping Project — Job Listing Scraper using Python & BeautifulSoup
