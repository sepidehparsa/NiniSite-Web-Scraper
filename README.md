
A Python script designed to scrape questions from the NiniSite website based on various psychological hashtags. This tool can gather relevant questions to analyze trends in mental health discussions.

## Background

This project aims to collect and analyze questions from NiniSite, which serves as a platform for discussions related to mental health, relationships, and personal development. The collected data can provide insights into common topics and concerns in these areas.

## Features

- **Scraping Functionality**: Efficiently collect questions related to mental health from NiniSite using specified psychological hashtags such as `#mentalhealth`, `#relationships`, and more.
- **Supports Pagination**: Automatically navigates through multiple pages to gather the desired number of links.
- **Data Output**: Saves the collected question links in both Excel and CSV formats for easy analysis and accessibility.

## Installation

To run this project, you will need Python installed on your machine. Follow these steps to set up the environment:

1. **Clone the repository or download the source code**:
   ```bash
   git clone https://github.com/sepidehparsa/NiniSite-Web-Scraper.git
   ```

2. **Navigate into the project directory**:
   ```bash
   cd NiniSite-Web-Scraper
   ```

3. **Install the required Python packages with pip**:
   ```bash
   pip install requests beautifulsoup4 pandas openpyxl
   ```

## Usage

To use the script, follow these steps:

1. Ensure you are in the project directory where the script is located.
2. Run the script using Python:
   ```bash
   python scraping_script.py
   ```

3. Upon successful execution, two output files will be generated in the same directory:
   - `question_links_grouped_with_urls.xlsx`: An Excel file containing the collected question links along with their associated hashtags.
   - `question_links_grouped_with_urls.csv`: A CSV file in a similar format for easy access and analysis with data tools.

## Example Output

After running the script, you will see the output files:
- **Excel File**: `question_links_grouped_with_urls.xlsx`, structured with columns for hashtags, their IDs, and the collected links.
- **CSV File**: `question_links_grouped_with_urls.csv`, providing the same information in a plain text format.

## Code Overview

### Main Components

- **Data Collection**: The script uses the `requests` library to fetch webpage content from NiniSite.
- **HTML Parsing**: The `BeautifulSoup` library is used to parse the HTML and extract relevant question links based on hashtags.
- **Storage**: Collected data is structured into a DataFrame using `pandas` and saved to Excel and CSV formats.

### Code Example

Here’s a snippet of the main scraping logic from the script to illustrate its functionality:

```python
import requests
from bs4 import BeautifulSoup
import re

def scrape_question_links(page_content):
    soup = BeautifulSoup(page_content, "html.parser")
    question_links = []
    
    for link in soup.find_all("a", href=True):
        href = link["href"]
        if re.match(r"^/clinic/question/\d+/.+", href):
            full_url = f"https://www.ninisite.com{href}"
            question_links.append(full_url)
    
    return question_links
```

## Contributing

Contributions to the project are encouraged. If you find any issues or have suggestions for improvements, please open an issue or submit a pull request. Your input can help improve this project for others.

### Contact

For questions, feedback, or inquiries regarding the project, feel free to reach out via email: [sepide95psy@gmail.com](mailto:sepide95psy@gmail.com).

## License

This project is licensed under the MIT License. For license details, refer to the [LICENSE](LICENSE) file included in this repository.

## Acknowledgments

- **NiniSite**: Acknowledging the platform for providing valuable content for individuals seeking guidance on mental health.
- **BeautifulSoup & Requests**: Thanks to the communities behind these libraries for creating tools that facilitate web scraping and data manipulation effectively.
```

### Key Points:
1. **Hashtag Example**: In the Features section, I included a reference to common psychological hashtags. You might want to customize this further based on the specific hashtags your script targets.
2. **Customization**: Make sure to replace `[your.email@example.com](mailto:your.email@example.com)` with your actual email.
3. **Organization**: The overall structure is maintained to ensure clarity and easy navigation for users interested in your project.

### How to Use:
- Copy and paste the text above into your `README.md` file on your GitHub repository.
- Review and make any necessary adjustments for your specific context or additional details.

This README should provide comprehensive information and guide users effectively. If you have any more questions or need further assistance, just let me know!
