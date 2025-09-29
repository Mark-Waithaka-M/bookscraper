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

## ⚙️ Setup Instructions

### 1. Clone the repo
git clone https://github.com/Mark-Waithaka-M/bookscraper.git
cd bookscraper

2. Create and activate virtual environment
python -m venv venv

source venv/bin/activate       # macOS/Linux
venv\Scripts\activate          # Windows

4. Install dependencies
pip install -r requirements.txt

6. Add environment variables
Create a .env file in the project root:

# Proxy credentials
PROXY_USER=your_proxy_username
PROXY_PASSWORD=your_proxy_password
PROXY_ENDPOINT=gate.smartproxy.com
PROXY_PORT=10001

# ScrapeOps API Key
SCRAPEOPS_API_KEY=your_scrapeops_api_key

# Example: OpenAI Key
OPENAI_API_KEY=your_openai_key_here

5. Run the spider
scrapy crawl bookspider -o books.json

🗄️ Database Support
The scraper can store data into:

MySQL (default)
PostgreSQL (optional)
ChromaDB (optional, for similarity search)

Check pipelines.py for database configurations.

🔑 Environment & Security
Sensitive API keys and credentials are stored in .env

.env and venv/ are ignored via .gitignore

Do not push secrets to GitHub

🤝 Contributing
Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.
