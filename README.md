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

**🌏 International Users:** Prefer email or Telegram? Contact shiyang@pangolinfo.com  
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
