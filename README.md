# Amazon Scraper using Selectorlib 

A simple amazon scraper to extract product details and prices from Amazon.com using Python Requests and Selectorlib. 

There are two simple scrapers in this project. 
1. Amazon Product Page Scraper `amazon.py`
1. Amazon Search Results Page Scraper `searchresults.py`

## Usage

From a terminal 

1. Clone this project  `git clone https://github.com/scrapehero-code/amazon-scraper.git` and cd into it `cd amazon-scraper`
1. Add a Virtual Environment `python3 -m venv .venv` (Optional)
1. Activate the Virtual Environment `source .venv/bin/activate` (Optional) 
1. Install Requirements `pip3 install -r requirements.txt`

## Scrape Product Details from Product Page

1. Add Amazon Product URLS to [urls.txt](urls.txt)
1. Run `python3 amazon.py`
1. Get data from [output/product.jsonl](output/product.jsonl.jsonl)

## Scrape Products from Search Results

This scraper only scrapes product from the first page of search results

1. Add Amazon Product URLS to [search_results_urls.txt](search_results_urls.txt)
1. Run `python3 searchresults.py` or `python3 searchresults.py -removeAds` to run and not include the ads
1. Get data from [output/search_results_output.jsonl](output/search_results_output.jsonl)

## Check the output [readme](output/README.md)

## FAQ
**- I am seeing `\u*` before my outputs(for example in price)**
*This is a unicode symbol. For example: `\u00a3` is a UK pound sign, so `\u00a3250.00` would be `£250` if you encoded the unicode character.*

**- The URL output from `searchresults.py` is not a full URL**
*Add `https://www.amazon.co.uk` in front of it. (Or whatever amazon region you want to scrape, this example goes to .co.**uk**)*

