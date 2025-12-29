# RealEstateVOmit

RealEstateVOmit is a real estate data scraping and exploration project focused on collecting property listings and turning them into structured, analyzable datasets. It serves as a learning playground for web scraping, cleaning messy HTML, and turning data into usable artifacts like printable PDF reports.

---

## Live site

The current version of the app is live at:

👉 https://revom.vercel.app/

---

## Features

- Scrapes real estate listings from one or more target sites (e.g., listing portals or agency pages).
- Extracts core fields like title, price, location, bedrooms/bathrooms, and URL into a structured format (CSV, JSON, or a database).
- Handles multi-page result sets with simple pagination logic.
- Includes basic checks and filters to keep obviously bad or duplicate rows out of the final dataset.
- Builds PDF reports so selected properties can be shared as clean, printable summaries for agents and clients.

---

## Tech Stack

- **Language:** Python (scraping and data processing)  
- **Typical libraries:**
  - `requests` / `httpx` for HTTP requests
  - `BeautifulSoup` / `lxml` or a scraping framework (e.g., Scrapy) for HTML parsing
  - `pandas` for cleaning and exporting data
  - A PDF generation tool (e.g., HTML-to-PDF or a PDF library) for report creation
- **Storage:** CSV or SQLite for local experiments and quick analysis.
- **Frontend / app layer:** Deployed web app for browsing listings and triggering PDF generation, hosted on Vercel.

---

## Project Goals

- Build a repeatable pipeline to pull real estate data instead of copy‑pasting from websites.
- Explore questions like price ranges, distribution by neighborhood, or bedroom count using the scraped data.
- Provide a simple PDF builder so scraped data can be turned into a format that is easy to email or print for clients.
- Practice writing scrapers that are resilient to layout changes and respect target site constraints (rate limiting, timeouts, etc.).

---

## What I Implemented

- **Scraping pipeline**
  - Defined scraping logic for one or more real estate listing pages.
  - Selected listing cards and extracted fields (title, price, location, link, and other details).
  - Followed pagination links or page parameters to walk through multiple result pages.
  - Normalized and cleaned raw data into a consistent schema (e.g., stripping currency symbols, converting numbers, handling missing values).
  - Added simple duplicate detection so the same listing is not stored repeatedly.

- **PDF builder**
  - Built the PDF builder workflow to turn selected property data into a clean, printable report.
  - Connected scraped listing fields (price, address, features, images) into a PDF template.
  - Added basic layout and formatting controls so PDFs are readable and useful for agents and clients.

- **Integration & UX**
  - Helped connect the scraping output with the app UI so users can browse listings and trigger PDF generation.
  - Contributed to making the app feel like a coherent flow from data collection to client-ready output.

---

## What I Learned

- How to inspect page structure (HTML + network tab) and design selectors that survive minor layout changes.
- The importance of defensive scraping: handling missing fields, timeouts, and unexpected responses instead of crashing.
- Basic data-cleaning patterns for real estate (price normalization, area/bedroom parsing, handling inconsistent text).
- How to go from raw scraped data to a user-facing artifact (PDF) that is actually useful in real estate conversations.
- Practical tradeoffs in PDF layout: balancing detail versus readability on a single page or short report.

---

## How to Run (local scraping pipeline)

1. **Clone the repository**

```
git clone https://github.com/NaeemChakera/RealEstateVOmit.git
cd RealEstateVOmit
```

2. **Create and activate a virtual environment** (optional but recommended)
```
python -m venv .venv

macOS / Linux
source .venv/bin/activate

Windows
.venv\Scripts\activate
```
3. **Install dependencies**
```
pip install -r requirements.txt
```
4. **Configure settings**

Update configuration values (target URL, search parameters, output paths, PDF settings) in the config file or at the top of the main script.

5. **Run the scraper**
```
python main.py
```
6. **Generate or view PDFs**

- Use the app flow or script entry point for PDF generation (for example, a CLI flag or separate script like `python build_pdf.py`).  
- Open the generated PDF reports in your PDF viewer of choice.

---

## Acknowledgements

This project would not exist without my team, our reviewed ideas, and helped push it from a rough scraper into a working app. Their input shaped both the technical decisions and the overall direction of RealEstateVomit.






