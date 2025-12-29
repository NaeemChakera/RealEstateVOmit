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

- Built the PDF builder workflow to turn selected property data into a clean, printable report.
- Connected scraped listing fields (price, address, features, images) into a PDF template.
- Added basic layout and formatting controls so PDFs are readable for agents and clients.

---

## What I Learned

- How to go from raw scraped data to a user-facing artifact (PDF) that is useful in real estate conversations.
- Practical tradeoffs in PDF layout: balancing detail vs. readability on a single page or short report.
  
---

## How to Run

1. **Clone the repository**

