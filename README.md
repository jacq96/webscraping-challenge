# webscraping-challenge
12/15/2023- I did reach out to Tyler via email for assistance with a fix that had given for using Selenium instead of Splinter as it wasn't working for most of us.
Occasional errors that I couldn't diagnose myself were fixed by using ChatGPT. 
Otherwise consulted previous class materials from activities to work through coding struggles. 
Googled the amount of Earth days that are in a Martian year to have a reference point. 

Selenium Fix that was given during class: 
from selenium import webdriver
from selenium.webdriver.chrome.service import Service
from bs4 import BeautifulSoup
import os

current_directory = os.getcwd()
chromedriver_path = os.path.join(current_directory, '..', '..', 'chromedriver', 'chromedriver.exe')

# Set up Chrome options
chrome_options = webdriver.ChromeOptions()
# Uncomment the line below if you want the browser to run headless
# chrome_options.add_argument("--headless")

# Initialize the Chrome WebDriver with the updated method
service = Service(executable_path=chromedriver_path)
browser = webdriver.Chrome(service=service, options=chrome_options)
