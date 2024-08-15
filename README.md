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

import requests 
from urllib.parse import quote,unquote
import urllib.parse
import re
import unidecode
import pandas as pd

```

## How to Use

1. **Clone the Repository**:
   Clone this repository to your local machine using:
   ```bash
   git clone https://github.com/doreziagim/linkedin-contact-extractor.git
   ```

2. **Set Up the Environment**:
   Ensure that the required Python packages are installed as mentioned in the requirements section.

3. **Obtain LinkedIn Cookies**:
   - You will need your LinkedIn session cookies (`li_at` and `JSESSIONID`) to authenticate the API requests.
   - Log into LinkedIn via a web browser and use developer tools (F12) to find these cookies in the network requests.

4. **Configure Script Variables**:
   - Open the script in your preferred code editor.
   - Set the `li_at`, `JSESSIONID`, and `user` variables in the script with your LinkedIn session details and the LinkedIn username you want to scrape.

   ```python
   li_at = "your_li_at_cookie_value"
   JSESSIONID = "your_jsessionid_cookie_value"
   user = "target_linkedin_username"
   ```

5. **Run the Script**:
   Execute the script in your Python environment:
   ```bash
   python linkedin_contact_extractor.py
   ```

6. **Output**:
   - The script will return a pandas dataframe with the target user and their connections' information, including `userID`, `userCode`, `Name`, `JobPosition`, `ConnectionDegree`, `Location`, and `UserProfileLink`.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

## Disclaimer

This script is intended for educational and research purposes only. Use it responsibly and ensure compliance with LinkedIn's terms of service. Unauthorized scraping or data extraction from LinkedIn may result in your account being banned.
