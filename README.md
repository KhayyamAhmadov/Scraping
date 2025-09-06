# 🛒 Amazon Product Scraper  

This project is a **Python-based web scraper** for Amazon products. It uses **Selenium (with undetected-chromedriver)** and **BeautifulSoup** to collect product details such as:  

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
- Auto-handles **cookie consent popups**.  
- Scrolls and clicks **"Load more" buttons** to collect as many products as possible.  
- Extracts product details and customer reviews.  
- Saves data incrementally to prevent data loss.  
- Uses randomized delays to mimic human behavior.  

---

## 📦 Requirements  

Make sure you have **Python 3.11+** installed. Then install the required dependencies:  

```bash
pip install selenium beautifulsoup4 undetected-chromedriver tqdm

---

## ⚙️ How It Works
1. Opens Amazon category pages defined in the `url` list.  
2. Scrolls through the page and clicks "Load more" buttons until no new products appear.  
3. Collects product links and visits each product page.  
4. Extracts details (name, rating, reviews, etc.).  
5. Saves the data into `amazon_products.json`.  

---

## 📝 Code Structure
- `save_data()` → Saves scraped data into JSON file.  
- `url` list → Contains Amazon category URLs to scrape.  
- Product selectors → Extracts product links from category pages.  
- Load More logic → Scrolls and clicks "Load more" buttons to get more results.  
- Product page scraper → Collects details such as name, rating, category, description, reviews.  
- Incremental save → Data is saved automatically after every 10 products.

---

## 📂 Output Example

{
  "URL": "https://www.amazon.com/dp/example",
  "Name": "Sample Product Title",
  "Star_Rating": "4",
  "Product_Ratings": "12,345 ratings",
  "Category": "Electronics › Computers & Accessories",
  "Description": "This is a sample product description with features...",
  "Reviews": [
    {
      "Review": "Great product, works perfectly!",
      "Rating": 5.0
    },
    {
      "Review": "Not worth the price.",
      "Rating": 2.0
    }
  ]
}

