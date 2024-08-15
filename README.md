# linkedin-contact-extractor
The LinkedIn Contact Extractor is a Python script designed to automate the extraction and cleaning of contact information from a LinkedIn profile. This tool uses the LinkedIn API to fetch details about a user's connections and presents the data in a clean and structured format.

# LinkedIn Contact Extractor

## Overview

The LinkedIn Contact Extractor is a Python script designed to automate the extraction and cleaning of contact information from a LinkedIn profile. This tool uses the LinkedIn API to fetch details about a user's connections and presents the data in a clean and structured format. 

## Features

- **Text Normalization**: Cleans and normalizes text data, including removing emojis and other unicode icons, handling German umlauts, and removing diacritics.
- **Employee Information Extraction**: Extracts key information about a specific LinkedIn user, such as their name, position, location, profile link, and connection degree.
- **Contact Information Retrieval**: Iteratively gathers information about a user's connections, compiling it into a structured dataframe.

## Requirements

Before running the script, ensure you have the following Python libraries installed:

```bash
pip install requests pandas unidecode
