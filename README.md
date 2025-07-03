# MPEP-Chatbot

MPEP-Chatbot is a tool that converts the Manual of Patent Examining Procedure (MPEP) from the USPTO's Reference Document Management System (RDMS) into a structured JSON format and utilizes LlamaIndex to create an interactive chatbot. This enables users to query and interact with MPEP content seamlessly. It was demo'ed on an airgapped laptop at USPTO Community Day 2024 using a Microsoft Phi LLM.

## Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## Features

- **Automated Scraping**: Utilizes Selenium to extract MPEP content from the RDMS.
- **HTML to JSON Conversion**: Parses HTML content using Beautiful Soup and converts it into a clean JSON format.
- **Interactive Chatbot**: Employs LlamaIndex to create a chatbot for querying MPEP content.

## Prerequisites

Before using MPEP-Chatbot, ensure you have the following installed:

- **Python 3.x**: The core programming language for running the scripts.
- **Jupyter Notebook**: To execute `.ipynb` files.
- **Selenium**: For web scraping purposes.
- **Beautiful Soup 4**: For parsing HTML content.
- **ChromeDriver**: Compatible with your version of Google Chrome.
- **LlamaIndex**: For building the chatbot interface.

## Installation

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/USPTOCode/MPEP-Chatbot.git
   cd MPEP-Chatbot
   ```

2. **Set Up Virtual Environment** (Optional but recommended):

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Required Packages**:

   ```bash
   pip install -r requirements.txt
   ```

4. **Download ChromeDriver**:

   - Visit the [ChromeDriver download page](https://chromedriver.chromium.org/) to get the latest version.
   - Ensure compatibility between ChromeDriver and your installed version of Google Chrome.
   - Optionally, refer to [Chrome for Testing (CfT)](https://developer.chrome.com/blog/chrome-for-testing) for more details.
   - Find the appropriate CfT version [here](https://github.com/GoogleChromeLabs/chrome-for-testing#json-api-endpoints).

5. **Configure ChromeDriver Path**:

   Ensure that the `chromedriver` executable is in your system's PATH or specify its location in the scripts.

## Usage

1. **Run the Selenium Scraper**:

   Open and execute the `rdms_selenium_scraper.ipynb` notebook to scrape MPEP content from the RDMS.

2. **Convert HTML to JSON**:

   Execute the `html_to_json_bs4parser.ipynb` notebook to parse the scraped HTML and generate a consolidated JSON file.

3. **Build the Chatbot with LlamaIndex**:

   Open and run the `llama_indexer.ipynb` notebook to create an interactive chatbot using the processed MPEP data.


## License

This project is licensed under the [MIT License](LICENSE).


