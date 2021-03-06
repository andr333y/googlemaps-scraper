# Google Maps Scraper
Scraper of Google Maps reviews.
The code allows to extract the **most recent** reviews starting from the url of a specific Point Of Interests (POIs) in Google Maps.


## Installation
Follow these steps to use the scraper:
- Download Chromedrive from [here](https://chromedriver.storage.googleapis.com/index.html?path=2.45/).
- Install Python packages from requirements file, either using pip, conda or virtualenv:

        conda create --name scraping python=3.6 --file requirements.txt

**Note**: Python >= 3.6 is required. 

## Usage
The scraper needs two main parameters as input:
- `--i`: input file name, containing a list of urls that point to Google Maps place reviews (default: _urls.txt_)
- `--N`: number of reviews to retrieve, starting from the most recent (default: 100)

Example:

  `python scraper.py --N 50`
 
generates a csv file containing last 50 reviews of places present in _urls.txt_

In current implementation, the CSV file is handled as an external function, so if you want to change path and/or name of output file, you need to modify that function.

Additionally, other two parameters can be provided:
- `--place`: boolean value that allows to scrape POI metadata instead of reviews (default: false)
- `--debug`: boolean value that allows to run the browser using the graphical interface (default: false)
