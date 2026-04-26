# Python Automation: Learning Guide
## Section Index
1. [What is Python Automation?](#1-what-is-python-automation)
2. [Why Python is Good for Automation](#2-why-python-is-good-for-automation)
3. [Automation Thinking: Input → Process → Output](#3-automation-thinking-input--process--output)
4. [Environment Setup](#4-environment-setup)
5. [File and Folder Automation](#5-file-and-folder-automation)
6. [Data Cleaning and Excel Report Automation](#6-data-cleaning-and-excel-report-automation)
7. [Task Scheduling Automation](#7-task-scheduling-automation)
8. [Web Data / API Automation](#8-web-data--api-automation)
9. [Web Scraping Automation](#9-web-scraping-automation)
10. [Email Automation](#10-email-automation)
11. [GUI / Desktop Automation](#11-gui--desktop-automation)
12. [Error Handling, Logging, and Configuration](#12-error-handling-logging-and-configuration)
13. [Advanced Automation Architecture](#13-advanced-automation-architecture)
14. [AI, ML, and Cloud Automation Ideas](#14-ai-ml-and-cloud-automation-ideas)
15. [Portfolio Project Ideas](#15-portfolio-project-ideas)
16. [Quick Cheat Sheet](#16-quick-cheat-sheet)
17. [Final Learning Path](#final-learning-path)
18. [Best Final Project Idea](#best-final-project-idea)
---

## 1. What is Python Automation?

Python automation means using Python scripts to do repetitive tasks automatically.

Examples:

- Rename many files
- Move files into folders
- Clean CSV or Excel data
- Generate reports
- Send emails
- Fetch API data
- Scrape websites
- Schedule daily tasks
- Run ETL/data pipelines
- Trigger AI/ML decisions

Python is useful because it has simple syntax and many libraries for files, data, scheduling, web automation, APIs, and cloud workflows.

---

## 2. Why Python is Good for Automation

Python is popular for automation because:

- Code is readable and beginner-friendly
- It has many built-in libraries
- It works on Windows, Linux, and macOS
- It can connect with files, databases, APIs, browsers, email, and cloud services
- It can scale from simple scripts to advanced data engineering workflows

Common useful libraries:

| Task | Libraries |
|---|---|
| File automation | `os`, `shutil`, `pathlib` |
| Data automation | `pandas`, `openpyxl` |
| Scheduling | `schedule`, `APScheduler` |
| Web requests | `requests` |
| Web scraping | `BeautifulSoup`, `Scrapy` |
| Browser automation | `Selenium`, `Playwright` |
| Email automation | `smtplib`, `email` |
| Desktop GUI automation | `pyautogui` |
| Workflow orchestration | `Apache Airflow` |

---

## 3. Automation Thinking: Input → Process → Output

Every automation script can be understood like this:

```text
Input  →  Process  →  Output
````

Example:

```text
CSV file  →  Clean data  →  Excel report
Images    →  Analyze     →  Save results
API data  →  Transform   →  Dashboard table
Folder    →  Organize    →  Clean directory
```

This model makes your automation easier to design.

---

## 4. Environment Setup

Create a project folder:

```bash
mkdir python-automation-practice
cd python-automation-practice
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

Activate it on Linux/macOS:

```bash
source venv/bin/activate
```

Install useful packages:

```bash
pip install pandas openpyxl requests beautifulsoup4 schedule python-dotenv
```

Recommended project structure:

```text
python-automation-practice/
│
├── data/
│   ├── input/
│   └── output/
│
├── logs/
│
├── scripts/
│   ├── file_organizer.py
│   ├── data_report.py
│   ├── api_fetcher.py
│   └── email_sender.py
│
├── .env
├── requirements.txt
└── README.md
```

Save installed packages:

```bash
pip freeze > requirements.txt
```

---

## 5. File and Folder Automation

### Goal

Automatically organize files by type.

Example:

```text
Downloads/
├── invoice.pdf
├── photo.jpg
├── data.csv
├── notes.txt
```

After automation:

```text
Organized/
├── PDFs/
├── Images/
├── CSVs/
└── Text/
```

### Code: File Organizer

```python
from pathlib import Path
import shutil

# Source folder: change this to your real folder
source_folder = Path("data/input")

# Destination main folder
destination_folder = Path("data/output/organized")

# File type mapping
file_categories = {
    "PDFs": [".pdf"],
    "Images": [".jpg", ".jpeg", ".png"],
    "CSVs": [".csv"],
    "Text": [".txt"],
    "Excel": [".xlsx", ".xls"]
}

# Create destination folders if they do not exist
for category in file_categories:
    (destination_folder / category).mkdir(parents=True, exist_ok=True)

# Loop through every file in the source folder
for file_path in source_folder.iterdir():
    # Skip folders
    if file_path.is_dir():
        continue

    # Get file extension in lowercase
    extension = file_path.suffix.lower()

    # Move file based on extension
    moved = False

    for category, extensions in file_categories.items():
        if extension in extensions:
            target_path = destination_folder / category / file_path.name
            shutil.move(str(file_path), str(target_path))
            print(f"Moved: {file_path.name} → {category}")
            moved = True
            break

    # If file type does not match any category
    if not moved:
        other_folder = destination_folder / "Others"
        other_folder.mkdir(exist_ok=True)
        shutil.move(str(file_path), str(other_folder / file_path.name))
        print(f"Moved: {file_path.name} → Others")
```

### Run

```bash
python scripts/file_organizer.py
```

---

## 6. Data Cleaning and Excel Report Automation

### Goal

Read a CSV file, clean it, calculate summary values, and export an Excel report.

Example input file:

```text
data/input/sales.csv
```

Example columns:

```text
date,product,quantity,price
2026-04-01,Milk,10,1.50
2026-04-01,Bread,5,2.00
```

### Code: CSV to Clean Excel Report

```python
import pandas as pd
from pathlib import Path

# Input and output paths
input_file = Path("data/input/sales.csv")
output_file = Path("data/output/cleaned_sales_report.xlsx")

# Create output folder if it does not exist
output_file.parent.mkdir(parents=True, exist_ok=True)

# Read CSV data
df = pd.read_csv(input_file)

# Remove duplicate rows
df = df.drop_duplicates()

# Fill missing values
df = df.fillna(0)

# Create a new column: total sales
df["total_sales"] = df["quantity"] * df["price"]

# Create summary by product
summary = df.groupby("product", as_index=False)["total_sales"].sum()

# Save multiple sheets into one Excel file
with pd.ExcelWriter(output_file, engine="openpyxl") as writer:
    df.to_excel(writer, sheet_name="Cleaned_Data", index=False)
    summary.to_excel(writer, sheet_name="Summary", index=False)

print(f"Report created successfully: {output_file}")
```

### Why this is useful

This is useful for:

* Business reports
* Sales analysis
* Student projects
* Dashboard preparation
* Data engineering practice

---

## 7. Task Scheduling Automation

Python scripts can be scheduled using:

* Windows Task Scheduler
* Linux/macOS cron
* Python `schedule` library
* `APScheduler` for more advanced scheduling

Use `schedule` for simple repeated tasks. Use `APScheduler` when you need more advanced timing, persistence, or production-style workflows.

### Code: Run a Job Every Day

```python
import schedule
import time
from datetime import datetime

def daily_job():
    """This function runs automatically based on the schedule."""
    print(f"Running daily job at {datetime.now()}")

    # Example task:
    # 1. Read data
    # 2. Clean data
    # 3. Create report
    # 4. Send email

# Run every day at 08:00
schedule.every().day.at("08:00").do(daily_job)

print("Scheduler started...")

while True:
    # Check if any scheduled job should run
    schedule.run_pending()

    # Wait 60 seconds before checking again
    time.sleep(60)
```

### Important

This script must keep running. For real production use, use:

* Windows Task Scheduler
* cron
* Docker container
* Cloud Functions
* Cloud Run Jobs
* Airflow

---

## 8. Web Data / API Automation

### Goal

Fetch data from an API and save it as a CSV file.

APIs are usually better than scraping because they provide structured data.

### Code: Fetch API Data

```python
import requests
import pandas as pd
from pathlib import Path

# Example public API
url = "https://jsonplaceholder.typicode.com/posts"

# Send GET request
response = requests.get(url, timeout=10)

# Stop if request failed
response.raise_for_status()

# Convert JSON response to Python list/dict
data = response.json()

# Convert data to DataFrame
df = pd.DataFrame(data)

# Save output
output_file = Path("data/output/api_posts.csv")
output_file.parent.mkdir(parents=True, exist_ok=True)

df.to_csv(output_file, index=False)

print(f"API data saved to: {output_file}")
```

### Use cases

* Weather data automation
* Product price tracking
* Open data collection
* Dashboard data refresh
* IoT/robot sensor data collection

---

## 9. Web Scraping Automation

### Important Rule

Use an official API when available. Scraping can break if the website layout changes. Always check the website’s terms of service before scraping.

### Code: Simple Web Scraper

```python
import requests
from bs4 import BeautifulSoup

url = "https://example.com"

# Fetch webpage HTML
response = requests.get(url, timeout=10)
response.raise_for_status()

# Parse HTML
soup = BeautifulSoup(response.text, "html.parser")

# Extract page title
title = soup.find("h1")

if title:
    print("Page title:", title.get_text(strip=True))
else:
    print("No h1 title found.")
```

### Better use cases

* Scrape your own website
* Scrape public test pages
* Extract product names for learning
* Extract article titles for practice

Avoid scraping private, protected, or restricted content.

---

## 10. Email Automation

### Goal

Send an automated email using Python.

Common uses:

* Send monthly reports
* Send system alerts
* Send job status notifications
* Send error messages from automation scripts

### Security Note

Do not write your email password directly inside Python code. Use environment variables.

Create a `.env` file:

```env
EMAIL_ADDRESS=your_email@gmail.com
EMAIL_PASSWORD=your_app_password
EMAIL_RECEIVER=receiver@example.com
```

### Code: Send Email Safely

```python
import os
import smtplib
from email.message import EmailMessage
from dotenv import load_dotenv

# Load variables from .env file
load_dotenv()

email_address = os.getenv("EMAIL_ADDRESS")
email_password = os.getenv("EMAIL_PASSWORD")
email_receiver = os.getenv("EMAIL_RECEIVER")

# Create email message
msg = EmailMessage()
msg["Subject"] = "Python Automation Report"
msg["From"] = email_address
msg["To"] = email_receiver
msg.set_content("Hello, this is an automated email from Python.")

# Connect to SMTP server
with smtplib.SMTP("smtp.gmail.com", 587) as server:
    server.starttls()

    # Login using app password
    server.login(email_address, email_password)

    # Send email
    server.send_message(msg)

print("Email sent successfully.")
```

### Gmail note

For Gmail, use an **App Password**, not your normal Gmail password.

---

## 11. GUI / Desktop Automation

GUI automation means controlling mouse, keyboard, and desktop apps automatically.

Useful library:

```bash
pip install pyautogui
```

### Code: Simple Desktop Automation

```python
import pyautogui
import time

# Wait 3 seconds so you can switch to another window
time.sleep(3)

# Type text automatically
pyautogui.write("Hello from Python automation!", interval=0.05)

# Press Enter
pyautogui.press("enter")
```

### Use cases

* Repetitive desktop actions
* Simple Excel UI tasks
* Form filling practice
* Testing desktop interfaces

### Warning

GUI automation is fragile because it depends on screen position, window layout, and timing.

---

## 12. Error Handling, Logging, and Configuration

Good automation should not crash silently.

It should:

* Catch expected errors
* Log useful information
* Use environment variables
* Avoid hardcoded passwords
* Fail clearly when something is wrong

### Code: Logging Example

```python
import logging
from pathlib import Path

# Create logs folder
Path("logs").mkdir(exist_ok=True)

# Configure logging
logging.basicConfig(
    filename="logs/automation.log",
    level=logging.INFO,
    format="%(asctime)s - %(levelname)s - %(message)s"
)

def divide_numbers(a, b):
    try:
        result = a / b
        logging.info(f"Division successful: {a} / {b} = {result}")
        return result

    except ZeroDivisionError:
        logging.error("Cannot divide by zero.")
        return None

    finally:
        logging.info("divide_numbers function finished.")

answer = divide_numbers(10, 0)
print(answer)
```

### Best practices

* Use `try/except` for expected errors
* Use `finally` for cleanup
* Use `logging`, not only `print`
* Use `.env` for secrets
* Use clear error messages
* Use efficient libraries like `pandas`
* Use batching for large tasks
* Use profiling tools when code is slow

---

## 13. Advanced Automation Architecture

For bigger automation systems, you need more than one script.

### 13.1 APScheduler

Use APScheduler when you need:

* Cron-style scheduling
* Background jobs
* Persistent jobs
* Better production control

Example use cases:

* Daily report generation
* Scheduled email sending
* Health checks
* Database cleanup
* ETL jobs

### 13.2 Apache Airflow

Use Airflow when your workflow has many steps.

Example workflow:

```text
Download data
    ↓
Clean data
    ↓
Train ML model
    ↓
Save predictions
    ↓
Update dashboard
    ↓
Send email report
```

Airflow is useful for:

* Data engineering
* ETL pipelines
* ML pipelines
* Scheduled reporting
* Monitoring workflow failures

### 13.3 Cloud Automation

Cloud automation means running scripts without managing your own server.

Examples:

* AWS Lambda
* Google Cloud Functions
* Azure Functions
* Google Cloud Run Jobs

Use cloud automation when you want:

* Automatic scaling
* Event-based execution
* Less server management
* Pay-per-use compute

---

## 14. AI, ML, and Cloud Automation Ideas

Modern automation can include AI and ML.

Examples:

### AI Report Generator

```text
Input: CSV sales data
Process: Analyze + summarize with AI
Output: Text report
```

### ML Predictive Maintenance

```text
Input: Sensor data
Process: ML model predicts failure risk
Output: Maintenance alert
```

### Food Demand Forecasting

```text
Input: Daily cafeteria sales
Process: ML model predicts tomorrow demand
Output: Dashboard + cooking recommendation
```

### Robotics Automation

```text
Input: Camera image
Process: Object detection
Output: Robot pick-and-place command
```

### Smart Grocery Scanner

```text
Input: Food/product image
Process: AI analysis
Output: Freshness/safety result
```

---

## 15. Portfolio Project Ideas

### Project 1: Smart File Organizer

Build a Python script that organizes files by type, date, or project name.

Skills shown:

* File handling
* Automation logic
* Clean folder structure
* Logging

---

### Project 2: Automated Excel Report Generator

Build a script that reads CSV data, cleans it, creates summaries, and exports Excel reports.

Skills shown:

* pandas
* openpyxl
* Data cleaning
* Report automation

---

### Project 3: Daily Weather Data Collector

Fetch weather data every day from an API and save it to CSV or database.

Skills shown:

* API automation
* Scheduling
* Data storage
* Dashboard preparation

---

### Project 4: Email Report Bot

Generate a report and automatically send it by email.

Skills shown:

* SMTP
* Environment variables
* Attachments
* Scheduling

---

### Project 5: Mini ETL Pipeline

Create a full automation pipeline:

```text
CSV/API input → Clean data → Save database/CSV → Generate report → Send email
```

Skills shown:

* ETL
* Data engineering
* Error handling
* Automation architecture

---

## 16. Quick Cheat Sheet

### File handling

```python
from pathlib import Path

folder = Path("data/input")

for file in folder.iterdir():
    print(file.name)
```

### Move file

```python
import shutil

shutil.move("old/file.txt", "new/file.txt")
```

### Read CSV

```python
import pandas as pd

df = pd.read_csv("data.csv")
```

### Save Excel

```python
df.to_excel("report.xlsx", index=False)
```

### API request

```python
import requests

response = requests.get("https://api.example.com/data")
data = response.json()
```

### Schedule job

```python
import schedule

schedule.every().day.at("08:00").do(my_function)
```

### Send email

```python
import smtplib
from email.message import EmailMessage
```

### Logging

```python
import logging

logging.info("Task completed.")
logging.error("Something went wrong.")
```

---

# Final Learning Path

## Beginner

1. File organizer
2. CSV cleaner
3. Excel report generator

## Intermediate

4. API data collector
5. Email report sender
6. Scheduled automation script

## Advanced

7. ETL pipeline
8. Airflow workflow
9. Cloud Function / Cloud Run Job
10. AI/ML automation project

---

# Best Final Project Idea

Build this:

```text
Automated Data Report System
```

Features:

1. Read CSV or API data
2. Clean data using pandas
3. Generate Excel report
4. Save logs
5. Send email automatically
6. Schedule daily execution

This project is simple, useful, and strong for ICT automation, data engineering, and AI/ML career preparation.

```

Key idea: start with **file + data automation**, then add **scheduling**, then add **email/API**, and finally connect it to **cloud or AI/ML**. DataCamp also emphasizes reliability practices like specific error handling, logging, environment variables for secrets, performance optimization, batching, and profiling. :contentReference[oaicite:1]{index=1}
::contentReference[oaicite:2]{index=2}
```

[1]: https://www.datacamp.com/tutorial/python-automation "Python Automation: A Complete Guide | DataCamp"
