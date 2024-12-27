# NiniSite Web Scraper  

A Python script designed to scrape questions from the NiniSite website based on various psychological hashtags. This tool can gather relevant questions to analyze trends in mental health discussions.  

## Background  

This project aims to collect and analyze questions from NiniSite, which serves as a platform for discussions related to mental health, relationships, and personal development. The collected data can provide insights into common topics and concerns in these areas.  

## Features  

- **Scraping Functionality**: Efficiently collect questions related to mental health from NiniSite using specified hashtags.  
- **Supports Pagination**: Automatically navigates through multiple pages to gather the desired number of links.  
- **Data Output**: Saves the collected question links in both Excel and CSV formats for easy analysis and accessibility.  

## Installation  

To run this project, you will need Python installed on your machine. Follow these steps to set up the environment:  

1.Clone the repository or download the source code:  

   ```bash  
   git clone https://github.com/sepidehparsa/NiniSite-Web-Scraper.git
2.Navigate into the project directory:
cd NiniSite-Web-Scraper
3.Install the required Python packages with pip:
pip install requests beautifulsoup4 pandas openpyxl

Usage
To use the script, follow these steps:

1.Ensure you are in the project directory where the script is located.

2.Run the script using Python:
python scraping_script.py
3.Upon successful execution, two output files will be generated in the same directory:

question_links_grouped_with_urls.xlsx: An Excel file containing the collected question links along with their associated hashtags.
question_links_grouped_with_urls.csv: A CSV file in a similar format for easy access and analysis with data tools.

  Contributing
Contributions to the project are encouraged. If you find any issues or have suggestions for improvements, please open an issue or submit a pull request. Your input can help improve this project for others.

Contact
For questions, feedback, or inquiries regarding the project, feel free to reach out via email: goodbookspublishinghouse@proton.me

  
