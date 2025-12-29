# RealEstateVOmit DevNet Project 1

RealEstateVOmit is a real estate data scraping and exploration project focused on collecting property listings and turning them into structured, analyzable datasets.[web:46] It serves as a learning playground for web scraping, cleaning messy HTML, and experimenting with basic real-estate analytics.[web:45]

---

## Features

- Scrapes real estate listings from one or more target sites (e.g., listing portals or agency pages).[web:46]
- Extracts core fields like title, price, location, bedrooms/bathrooms, and URL into a structured format (CSV, JSON, or a database).[web:45]
- Handles multi-page result sets with simple pagination logic.[web:45]
- Includes basic sanity checks and filters to keep obviously bad or duplicate rows out of the final dataset.[web:45][web:46]

---

## Tech Stack

- **Language:** Python  
- **Typical libraries:**
  - `requests` or `httpx` for HTTP requests
  - `BeautifulSoup` / `lxml` or a scraping framework (e.g., Scrapy) for HTML parsing
  - `pandas` for cleaning and exporting data
- **Storage:** CSV or SQLite for local experiments and quick analysis.[web:45][web:46]

---

## Project Goals

- Build a repeatable pipeline to pull real estate data instead of copy‑pasting from websites.[web:46]
- Explore questions like price ranges, distribution by neighborhood, or bedroom count using the scraped data.[web:46]
- Practice writing scrapers that are resilient to layout changes and respect target site constraints (rate limiting, timeouts, etc.).[web:45][web:46]

---

## What I Implemented

- Defined scraping logic for one or more real estate listing pages, including:
  - Selecting listing cards and extracting fields (title, price, location, link, etc.).[web:46]
  - Following pagination links or page parameters to walk through multiple result pages.[web:46]
- Normalized and cleaned raw data into a consistent schema (e.g., stripping currency symbols, converting numbers, handling missing values).[web:45]
- Added simple duplicate detection so the same listing is not stored repeatedly.[web:45]
- Exported the resulting dataset to CSV/SQLite for further analysis in notebooks or other tools.[web:45][web:46]

---

## What I Learned

- How to inspect page structure (HTML + network tab) and design selectors that survive minor layout changes.[web:46]
- The importance of defensive scraping: handling missing fields, timeouts, and unexpected responses instead of crashing.[web:45]
- Basic data-cleaning patterns for real estate (price normalization, area/bedroom parsing, handling inconsistent text).[web:45]
- How even a simple dataset unlocks useful questions about a market once it is in a structured format.[web:45][web:46]

---

## How to Run

1. **Clone the repository**

