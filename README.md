# 🛒 Amazon Product Scraper

This project is a Python-based web scraper for Amazon products. It uses **Selenium (with undetected-chromedriver)** and **BeautifulSoup** to collect product details such as:  

- Product name  
- Star rating  
- Number of ratings  
- Category (breadcrumb)  
- Description  
- Reviews (with review text and star rating)  
- Product URL  

All collected data is saved into a **JSON file (`amazon_products.json`)**.  

---

## 🚀 Features

- Scrapes Amazon product listings from multiple categories.  
- Auto-handles cookie consent popups.  
- Scrolls and clicks "Load more" buttons to collect as many products as possible.  
- Extracts product details and customer reviews.  
- Saves data incrementally to prevent data loss.  
- Uses randomized delays to mimic human behavior.  

---

## 📦 Requirements

Make sure you have **Python 3.11+** installed. Then install the required dependencies:  

```bash
pip install selenium beautifulsoup4 undetected-chromedriver tqdm
