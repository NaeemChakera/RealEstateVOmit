# RealEstateVOmit

RealEstateVOmit is a real estate data scraping and exploration project focused on collecting property listings and turning them into structured, analyzable datasets.[web:46] It serves as a learning playground for web scraping, cleaning messy HTML, and turning data into usable artifacts like printable PDF reports.[web:45]

---

## Live site

The current version of the app is live at:

👉 [https://revom.vercel.app/](https://revom.vercel.app/)[web:44]

---

## Features

- Scrapes real estate listings from one or more target sites (e.g., listing portals or agency pages).[web:46]
- Extracts core fields like title, price, location, bedrooms/bathrooms, and URL into a structured format (CSV, JSON, or a database).[web:45]
- Handles multi-page result sets with simple pagination logic.[web:45]
- Includes basic sanity checks and filters to keep obviously bad or duplicate rows out of the final dataset.[web:45][web:46]
- Builds PDF reports so selected properties can be shared as clean, printable summaries for agents and clients.[web:44]

---

## Tech Stack

- **Language:** Python (scraping and data processing)  
- **Typical libraries:**
  - `requests` / `httpx` for HTTP requests
  - `BeautifulSoup` / `lxml` or a scraping framework (e.g., Scrapy) for HTML parsing
  - `pandas` for cleaning and exporting data
  - A PDF generation tool (e.g., HTML
