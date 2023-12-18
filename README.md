# Marketplace Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Marketplace Scraper](https://oxylabs.io/products/scraper-api/web/marketplace-scraper?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from any marketplace effortlessly. This brief guide explains how a Marketplace Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get marketplace results by providing your own URLs to our service. We can return the HTML for any marketplace you like.

#### Python code example

The example below illustrates how you can get [swappa.com](https://swappa.com/sneakers/air-jordans) marketplace results.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://swappa.com/sneakers/air-jordans'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/marketplace-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "\n\n\n\n\n\n\n\n<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.1//EN\" \"http://www.w3.org/TR/xhtml11/DTD/xhtml11. ... </html>",
      "created_at": "2023-12-18 11:32:57",
      "updated_at": "2023-12-18 11:32:58",
      "page": 1,
      "url": "https://swappa.com/sneakers/air-jordans",
      "job_id": "7142476830446991361",
      "status_code": 200
    }
  ]
}
```
With our Marketplace Scraper, you can smoothly extract public data from any e-commerce marketplace platforms. Gather necessary inventory details, including product price, customer feedback, or in-depth descriptions, to understand the market and maintain an edge over your competitors. Should you need any clarification, our support team is ready to assist you via live chat or you can email us at hello@oxylabs.io.
