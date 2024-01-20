# Hotel Information Web Scraping
## Overview
This Python script is designed for web scraping hotel information from specified URLs. It utilizes the requests library for making HTTP requests, BeautifulSoup for parsing HTML content, and Pandas for organizing the extracted data into a DataFrame. The script is tailored to extract details such as hotel name, location, amenities, price, available rooms, check-in/out information, and customer reviews.


# Functions
extract_hotel_info(url)

-Extracts hotel information from a given URL.

-Returns a Pandas DataFrame containing the extracted data.

extract_urls_from_json(json_string)

-Extracts hotel URLs from a JSON string.

-Returns a list of URLs.

append_new_urls(existing_urls, additional_urls)

-Combines existing URLs with new URLs.

-Returns an updated list of URLs.

run_all_and_display(json_string, existing_urls=None)

-Orchestrates the entire process:

-Extracts URLs from the JSON.

-Appends new URLs to existing ones.

-Iterates through each URL to extract hotel information.

-Concatenates individual DataFrames into a single DataFrame.

-Saves the updated DataFrame to a CSV file (output.csv).

-Prints a success message.


# Execution Example
## Example JSON string
json_string = '''
{"@context":"http://schema.org","@type":"ItemList", ... }
'''

## Call the function to run all and display the result
run_all_and_display(json_string)

# Notes
The CSV file (output.csv) serves as a persistent storage for collected data.
Ensure that the structure of the provided JSON aligns with the expected format for successful URL extraction.
Review the script for additional customization based on specific HTML structures of the targeted websites.
