# bookscraper

# 📚 BookScraper

A web scraping project built with [Scrapy](https://scrapy.org/) that extracts book information from [Books to Scrape](https://books.toscrape.com).  
The project demonstrates modern scraping techniques including:

- ✅ Proxy rotation with authentication
- ✅ Fake browser headers
- ✅ API key management with `.env`
- ✅ MySQL / PostgreSQL database storage
- ✅ (Optional) Vector database (ChromaDB) for semantic search

---

## 📂 Project Structure

web-scrapping-with-scrapy/
│
├── venv/ # Virtual environment (ignored by git)
├── scrapy.cfg # Scrapy configuration
├── .gitignore # Git ignore rules
├── .env # Environment variables (not pushed to git)
├── README.md # Project documentation
│
└── bookscraper/ # Scrapy project folder
├── bookscraper/ # Core project code
│ ├── items.py # Item models
│ ├── middlewares.py # Custom middlewares (proxy, headers, etc.)
│ ├── pipelines.py # Data processing & DB storage
│ ├── settings.py # Project settings
│ └── spiders/ # Spiders folder
│ └── bookspider.py # Main spider
│
└── init.py
