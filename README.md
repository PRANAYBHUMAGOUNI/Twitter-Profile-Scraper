# Twitter-Profile-Scraper

## Overview

The Twitter Profile Scraper is a Python-based tool that uses Selenium WebDriver to automate the process of logging into Twitter and scraping profile information from specified Twitter accounts. The scraped data includes the user's bio, following count, followers count, location, and website. The results are saved in a CSV file for easy access and analysis.

## Features

- Automates login to Twitter.
- Scrapes various profile details including bio, following count, followers count, location, and website.
- Handles unusual login activity verification.
- Saves scraped data to a CSV file.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Python 3.x installed on your machine.
- Microsoft Edge browser installed.
- Microsoft Edge WebDriver compatible with your browser version.
- Internet connection to access Twitter.

## Installation

1. **Clone the repository**  or create a new Python file and copy the code into it.

2. **Install required packages**:
   You need to install the necessary Python packages. You can do this using pip:
```bash
pip install selenium python-dotenv
```

3. **Set up WebDriver**:
- Download the Microsoft Edge WebDriver from [Microsoft's official site](https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/).
- Place the WebDriver executable in a known directory.

4. **Create a `.env` file**:
Create a `.env` file in the same directory as your script and add your Twitter credentials:
```bash
TWITTER_USERNAME=your_twitter_username
TWITTER_PASSWORD=your_twitter_password
TWITTER_EMAIL=your_email_for_verification
EDGE_DRIVER_PATH=path_to_your_edge_driver_executable
```

## Usage

1. **Run the script**:
Execute the script from your VScode or Jupyter Notebook


2. **Monitor Output**:
The script will log into Twitter and process each URL specified in the `TWITTER_URLS` list. It will print scraped data to the console and save it to `twitter_profiles.csv`.

3. **Check Results**:
After execution, check the `twitter_profiles.csv` file for the scraped data.

## Code Structure

The main components of the code include:

- **setup_driver()**: Initializes and configures the Microsoft Edge WebDriver.
- **login_to_twitter()**: Handles logging into Twitter with error handling for unusual activity verifications.
- **clean_url()**: Validates and formats Twitter URLs.
- **scrape_profile()**: Extracts profile information from a Twitter account.
- **extract_count()**: Retrieves follower/following counts based on specified labels.
- **save_to_csv()**: Saves scraped results into a CSV file.
- **main()**: Coordinates the entire scraping process.

## Troubleshooting

- Ensure that your credentials are correct in the `.env` file.
- Check if the WebDriver path is set correctly in the `.env` file.
- Make sure that you have internet access while running the script.








