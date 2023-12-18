# Binance Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Binance Scraper](https://oxylabs.io/products/scraper-api/web/binance?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Binance website effortlessly. This brief guide explains how an Binance Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Binance results by providing your own URLs to our service. We can return the HTML for any Binance page you like.

#### Python code example

The example below illustrates how you can get HTML of Binance page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.binance.com/en/markets/overview'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/binance-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!doctype html>\n<html dir=\"ltr\" lang=\"en\">\n<head>\n  <script id=\"OneTrust-sdk\" nonce=\"3367b6c3-c96b-4 ... </html>",
      "created_at": "2023-12-18 11:13:19",
      "updated_at": "2023-12-18 11:13:20",
      "page": 1,
      "url": "https://www.binance.com/en/markets/overview",
      "job_id": "7142471889049377793",
      "status_code": 200
    }
  ]
}
```
With our Binance Scraper, you can smoothly extract public data from any Binance web page. Accumulate crucial financial information, such as cryptocurrency prices, trading volumes, or market trends, to understand the crypto market better and stay ahead of your competitors. If you require support or have queries, our dedicated team is ready to assist you via live chat or you can even email us at hello@oxylabs.io.