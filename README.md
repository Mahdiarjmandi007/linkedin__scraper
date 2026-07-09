
![Python](https://img.shields.io/badge/Python-3.x-blue)
![Selenium](https://img.shields.io/badge/Selenium-Web%20Automation-green)
![Streamlit](https://img.shields.io/badge/Streamlit-UI-red)
# LinkedIn Job Scraper

A Python-based application that automates LinkedIn job searches and extracts job listings using Selenium and Streamlit.

The application allows users to search for jobs by title and location, collect job data automatically, and export results to CSV and SQLite databases.

## Features

- Search LinkedIn jobs by title and location
- Automated LinkedIn login using saved cookies
- Email verification system
- Interactive Streamlit user interface
- Extract job title, company name, location, work type, and job URL
- Export results to CSV
- Store results in SQLite database
- Firefox WebDriver automation with Selenium

## Technologies

- Python
- Selenium
- Streamlit
- SQLite
- Pandas
- Yagmail
- Firefox WebDriver (GeckoDriver)

## Workflow

1. User registration
2. Email verification
3. Job title and location selection
4. Automated LinkedIn search
5. Data extraction
6. CSV generation
7. SQLite database creation

## Output Fields

The scraper collects:

- Job Title
- Company Name
- Location
- Employment Type
- Job URL

## Project Structure

```text
linkedin_scraper
│
├── data_mine.py
├── gui.py
├── login_for_cookies.py
├── verify_code.py
├── loadings.py
├── requirements.txt
├── linkedin.exe
└── geckodriver.exe
```
## Configuration

Before running the application, you must provide your own credentials.

### LinkedIn Account

Open `login_for_cookies.py` and replace:

```python
username.send_keys("YOUR_LINKEDIN_EMAIL")

password.send_keys("YOUR_LINKEDIN_PASSWORD")
```

with your LinkedIn account credentials.

### Gmail Verification

Open `verify_code.py` and replace:

```python
yagmail.SMTP(
    "YOUR_GMAIL_ADDRESS",
    "YOUR_GOOGLE_APP_PASSWORD"
)
```
with your Gmail address and Google App Password.

## Setup

1. Install project dependencies

```bash
pip install -r requirements.txt
```


> Note: If two-factor authentication is enabled on your Google account, you must create a Google App Password before using the email verification feature.

2. Run the application

```bash
streamlit run gui.py
```


## Disclaimer

This project was created for educational and research purposes.

Users are responsible for complying with LinkedIn's Terms of Service and applicable laws when using this software.
