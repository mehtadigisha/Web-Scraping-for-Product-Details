# Web-Scraping-for-Product-Details

# Web Scraping Project - Amazon & Flipkart

## Project Overview
This project was an attempt to scrape product details (name, price, and rating) from Amazon and Flipkart using **ScraperAPI** and **BeautifulSoup** in Python. The objective was to enable users to search for a product and store the extracted details in an Excel file.

## Challenges Faced
Despite multiple attempts and different strategies, I was unable to successfully extract product details from both websites due to the following reasons:

### 1. **Amazon & Flipkart Blocking Requests**
   - Both Amazon and Flipkart actively block web scraping attempts using bot detection mechanisms.
   - Even when using ScraperAPI, some requests returned **403 Forbidden** or **Captcha challenges**, preventing data extraction.

### 2. **Dynamic Content Rendering**
   - Many product details on Amazon and Flipkart are dynamically loaded using JavaScript.
   - BeautifulSoup is unable to process JavaScript-rendered content without additional tools like Selenium or Puppeteer.

### 3. **Frequent Website Layout Changes**
   - The structure of the product listing pages on Flipkart and Amazon frequently changes.
   - CSS class names are dynamically generated, making it difficult to extract specific elements reliably.

### 4. **Rate Limiting & API Restrictions**
   - ScraperAPI enforces rate limits, leading to request failures if too many queries were made within a short time.
   - Even with random delays (2-5 seconds), access was occasionally restricted.

## Approaches Tried
1. **Using ScraperAPI with Different Parameters**
   - Added **render=true** for JavaScript rendering.
   - Used different country codes (e.g., `us`, `in`).
   - Included **custom User-Agent headers** to mimic real browsers.

2. **Modifying HTML Selectors**
   - Updated CSS selectors based on current website structure.
   - Tried alternative ways to locate product details (e.g., XPath, different HTML tags).

3. **Adding Random Delays to Avoid Rate Limiting**
   - Introduced random delays between requests (2-5 seconds).
   - Attempted session persistence to reduce repeated requests.

4. **Exploring Alternative Libraries**
   - Considered using **Selenium** for automated browsing (I haven't worked with those libraries, so they were not used).

## Conclusion
Unfortunately, due to strict anti-scraping mechanisms on both websites, I was unable to successfully extract product details. Alternative approaches such as **official APIs**, **third-party scraping services**, or **automated browsing tools (Selenium, Puppeteer, Playwright)** may be required for future attempts.

## Future Recommendations
- **Use Amazon’s Product Advertising API** for legally retrieving product details.
- **Implement browser automation** with Selenium or Puppeteer to bypass JavaScript-based content loading.
- **Leverage proxy rotation services** to minimize the chances of being blocked.

---
**Status:** ❌ Not Completed Successfully
