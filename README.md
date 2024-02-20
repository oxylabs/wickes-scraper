# Wickes Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Wickes Scraper](https://oxylabs.io/products/scraper-api/ecommerce/wickes?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Wickes website effortlessly. This brief guide showcases how Wickes Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Wickes results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Wickes page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.wickes.co.uk/bathroom/suites'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/wickes-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en\">\n\n\t<head>\n\t\t\n\n\n\n\n\n\n\n\n    <!-- OneTrust Cookies Consent Notice start f ... </html>",
      "created_at": "2024-02-20 12:42:47",
      "updated_at": "2024-02-20 12:42:48",
      "page": 1,
      "url": "https://www.wickes.co.uk/bathroom/suites",
      "job_id": "7165687230625780737",
      "status_code": 200
    }
  ]
}
```
With our Wickes Scraper, you can seamlessly gather public data from any Wickes web page. Harvest the necessary DIY tool information, such as price, customer ratings, or product specifications, to gain insights into the home improvement market and stay ahead of your competitors. If you have any queries, reach out to our support team via live chat or email us at hello@oxylabs.io.