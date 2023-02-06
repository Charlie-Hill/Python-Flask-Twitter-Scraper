# Twitter scraper (Flask wrapper for Twint)

This is a very basic Flask HTTP API that uses the Twint library to fetch tweets from a specific query and returns results in a JSON format.

I use an expanded version of this API for monitoring tweets & mentions relating to stock tickers that I am interested in tracking or analysing.

## Prerequisites
- Python 3.x installed
- pip installed

## Installation
1. Clone the repository
2. Navigate to the project directory
3. Run the following command to install the required packages:
```pip install -r requirements.txt```
4. Run the following command to start the API:
```python app.py```

## Usage
The API runs on `http://localhost:5000` by default. You can access the API using a tool like `curl` or through a browser.

### Endpoints
The API has a single endpoint `/getTweets` that accepts a search query parameter.
Example:
```http://localhost:5000/getTweets?query=kodal+minerals+#kod+£kod```

Example Output:
```
[
    {
        timestamp: "2023-02-04 20:43:49 GMT Standard Time",
        tweet: "Great to see @KodalMinerals on this list.  #Kod $Kod",
        username: "ExampleTwitterUser"
    },
    {
        timestamp: "2023-02-04 20:39:33 GMT Standard Time",
        tweet: "Huge moment for @KodalMinerals  After the wait throughout 2022, we are well and truly going to have a stellar 2023.  #Kod $Kod",
        username: "ExampleTwitterUser"
    },
    ...
]
```

This endpoint returns a JSON object containing the tweets that match the given search query.

## Libraries
The following libraries are used in this project:

<b>Flask</b>: A micro web framework for Python. https://github.com/pallets/flask

<b>Twint</b>: An advanced Twitter scraping tool written in Python that allows for scraping Tweets and information from Twitter profiles without using Twitter's API. https://github.com/twintproject/twint

## Contributing
Contributions are welcome. Feel free to open a pull request.