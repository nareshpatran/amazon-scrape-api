## ✨ Why Pangolin?

Traditional web scrapers break when websites update their HTML structure. **Pangolin adapts automatically.**

- ✅ **Zero Maintenance** — Our AI detects page changes and updates parsers automatically
- ✅ **99.9% Uptime** — Enterprise-grade infrastructure with automatic retry logic
- ✅ **No Proxies Needed** — Built-in anti-bot bypass (CAPTCHA, rate limits, fingerprinting)
- ✅ **Multi-Format Output** — Get data as JSON, HTML, or Markdown — whatever your app needs
- ✅ **Real-Time Data** — Fresh product prices, inventory, reviews in milliseconds

**Perfect for:** E-commerce sellers, price monitoring tools, market research, product analytics, and dropshipping businesses.

---

## 🎁 Get Started Free

**For Open Source Community:**

<table>
<tr>
<td width="50%">

### 🆓 What You Get
- ✅ **200 free API calls/month**
- ✅ Full parser template code (Go)
- ✅ Technical support via email
- ✅ No credit card required
- ✅ Access to all platforms

</td>
<td width="50%">

### 📝 How to Claim
1. **Contact us** via email or WeChat
   - Email: shiyang@pangolinfo.com
   - WeChat: `Pangolin-Scraper`
2. **Mention "GitHub Free Tier"** in your message
3. **Receive your API key** within 24 hours

</td>
</tr>
</table>

**🌏 International Users:** Prefer email or Telegram? Contact csm@pangolinfo.com  
**🇨🇳 中国用户：** 添加微信 `Pangolin-Scraper` 备注「GitHub免费额度」

---

## 🚀 Quick Start (3 Minutes)

### Step 1: Get Your API Key
[Claim your 200 free API calls](#-get-started-free)

### Step 2: Make Your First Request

**Python:**
```python
import requests

API_KEY = "your_free_api_key_here"

response = requests.post(
    "http://scrapeapi.pangolinfo.com/api/v1/scrape",
    headers={"Authorization": f"Bearer {API_KEY}"},
    json={
        "url": "https://www.amazon.com/dp/B0DYTF8L2W",
        "parserName": "amzProductDetail",
        "formats": ["json"]
    }
)

print(response.json())
```

**JavaScript:**
```javascript
const response = await fetch("http://scrapeapi.pangolinfo.com/api/v1/scrape", {
  method: "POST",
  headers: {
    "Authorization": `Bearer YOUR_API_KEY`,
    "Content-Type": "application/json"
  },
  body: JSON.stringify({
    url: "https://www.amazon.com/dp/B0DYTF8L2W",
    parserName: "amzProductDetail",
    formats: ["json"]
  })
});

const data = await response.json();
console.log(data);
```

**cURL:**
```bash
curl -X POST http://scrapeapi.pangolinfo.com/api/v1/scrape \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "url": "https://www.amazon.com/dp/B0DYTF8L2W",
    "parserName": "amzProductDetail",
    "formats": ["json"]
  }'
```

### Step 3: Parse the Response
```json
{
  "asin": "B0DYTF8L2W",
  "title": "Product Title Here",
  "price": 29.99,
  "rating": 4.5,
  "reviews": 1234,
  "imageUrl": "https://...",
  "inStock": true,
  ...
}
```

**🎉 That's it!** You're now scraping e-commerce data with zero infrastructure setup.

---
---

## 📊 What's Included?

| Feature | Open Source Parser | Free API (200 calls) | Paid API |
|---------|-------------------|---------------------|----------|
| **Parser Template Code** | ✅ Full access (Go) | ❌ | ❌ |
| **Monthly API Calls** | ∞ (self-hosted) | ✅ 200 free | ✅ Custom volume |
| **Supported Platforms** | Amazon search only | ✅ All platforms | ✅ All platforms |
| **Auto Page Structure Updates** | 🔧 Manual updates | ✅ Automatic | ✅ Automatic |
| **Anti-Bot Handling** | 🔧 DIY (proxies, CAPTCHA) | ✅ Built-in | ✅ Advanced |
| **Data Formats** | JSON only | JSON, HTML, Markdown | JSON, HTML, Markdown |
| **Support** | 💬 Community (GitHub) | ✅ Email support | ✅ Priority support |
| **Uptime SLA** | N/A (self-hosted) | 99% | 99.9% |
| **Use Case** | Learning, testing | Small projects | Production apps |

**💡 Recommendation:**
- **Learning web scraping?** → Start with open source parser
- **Building a side project?** → Use free API tier
- **Running a business?** → Upgrade to paid for reliability

---

## 🛠️ Supported Platforms & Data

<table>
<tr>
<td width="25%" align="center">
  <img src="https://logo.clearbit.com/amazon.com" width="64" height="64" alt="Amazon">
  <br><strong>Amazon</strong>
</td>
<td width="25%" align="center">
  <img src="https://logo.clearbit.com/walmart.com" width="64" height="64" alt="Walmart">
  <br><strong>Walmart</strong>
</td>
<td width="25%" align="center">
  <img src="https://logo.clearbit.com/shopify.com" width="64" height="64" alt="Shopify">
  <br><strong>Shopify</strong>
</td>
<td width="25%" align="center">
  <img src="https://logo.clearbit.com/ebay.com" width="64" height="64" alt="eBay">
  <br><strong>eBay</strong>
</td>
</tr>
</table>

### Amazon Data Fields (30+ fields)
- Product Details: ASIN, title, price, images, variants
- Rankings: Best Sellers Rank, category position
- Reviews: Rating, review count, top reviews
- Seller Info: FBA/FBM, seller name, shipping
- Inventory: Stock status, availability date

### Walmart, eBay, Shopify
Similar comprehensive data extraction for each platform.

📖 **Full API Documentation:** https://docs.pangolinfo.com/api-reference

---
---

## 💼 Real-World Use Cases

### 🛍️ For E-commerce Sellers
```python
# Monitor competitor prices daily
products = ["B08N5WRWNW", "B08L5VFJ2C", "B07ZPKN6YR"]

for asin in products:
    data = scrape_amazon_product(asin)
    if data['price'] < my_price:
        send_alert(f"Competitor lowered price: {data['title']}")
```

**Result:** Stay competitive by adjusting prices based on real-time market data.

---

### 📊 For Market Researchers
```javascript
// Analyze product trends in a category
const category = "Electronics > Headphones";
const results = await scrape_amazon_search(category, pages=10);

const avgPrice = results.reduce((sum, p) => sum + p.price, 0) / results.length;
const topBrands = getMostFrequent(results.map(p => p.brand));
```

**Result:** Generate market reports with pricing trends, top brands, and customer sentiment.

---

### 🤖 For SaaS Builders
```python
# Build a price drop notification service
def check_wishlist(user_id):
    wishlist = get_user_wishlist(user_id)
    
    for item in wishlist:
        current_price = scrape_product(item.url)['price']
        
        if current_price < item.target_price:
            send_email(user_id, f"Price drop alert: {item.name}")
```

**Result:** Create a valuable service without managing scraping infrastructure.

---

### 📈 For Data Scientists
```python
# Collect training data for price prediction models
import pandas as pd

data = []
for asin in asin_list:
    product = scrape_amazon_product(asin)
    data.append({
        'title': product['title'],
        'price': product['price'],
        'rating': product['rating'],
        'reviews': product['reviews'],
        'category': product['category']
    })

df = pd.DataFrame(data)
df.to_csv('amazon_products.csv')
```

**Result:** Build ML models with clean, structured e-commerce data.

---
