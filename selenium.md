# Selenium
## Preset
- Selenium was invented by Jason Huggins while working at ThoughtWorks in 2004
- Official docs: [Slenium Documentation](https://www.selenium.dev/documentation/overview/)

## Table of Contents

- [Introduction to Selenium ](#Introduction-to-selenium)
- [Setup and Installation](#setup-and-installation)
- [Basic Concepts](#basic-concepts)

## Introduction to Selenium

Selenium: Slenium is an open-source framework for automating web browsers. It supports multiple programming language and browsers.

- Web application testing
- Web scraping
- Browser automation
- Regression testing

### Selenium Components

- Selenium WebDriver: Core component for browser automation
- Selenium Grid: For parallel test execution across multiple machines
- Selenium IDE: Browser extension for record and playback

### Supported Languages

- Python
- Java
- C#
- JavaScript (Node.js)
- Ruby
- PHP

# Setup and Installation

### Python Installation

- Install Selenium:  
pip install selenium

- Install Webdriver Manager:   
pip install webdriver-manger

- For Specific browers:  
pip install chromedriver-autoinstaller

### Setup

This guide explains two ways to initialize a **Chrome WebDriver** in Selenium using Python.

1. Automatic Driver Management

```python
from selenium import webdriver
from selenium.webdriver.chrome.service import Service
from webdriver_manager.chrome import ChromeDriverManager 

# Automatic driver management
driver = webdriver.Chrome(service=Service(ChromeDriverManager().install()))

Explanation:
- webdriver_manager: Automatically downloads the correct version of ChromeDriver compatible with your installed Chrome browser.
- Service(ChromeDriverManager().install()):
  - ChromeDriverManager().install() downloads the driver and returns the path.
  - Service() wraps this path to use with Selenium WebDriver.
- webdriver.Chrome(): Launches the Chrome browser using the service provided.
```

2. Manual Driver path
```python
from selenium import webdriver
driver = webdriver.Chrome('/path/to/chromedriver')
```

# Basic Concepts

Selenium WebDriver is used to automate browser actions. Understanding its core concepts helps in writing effective automation scripts.

---
**WebDriver Interface**

- **Definition**: The `WebDriver` interface represents a browser instance in Selenium.  
- **Purpose**: It provides methods to control the browser, like opening a URL, navigating, or closing the browser.  
- **Example**:
```python
from selenium import webdriver
driver = webdriver.Chrome()  # Launches Chrome browser
driver.get("https://example.com")  # Opens the URL
driver.quit()  # Closes the browser
```
**Key Classes and Interfaces**
1. **WebDriver**
- Main interface for browser automation.
- Common methods:
    - get(url) – Open a web page.
    - back() – Go to the previous page.
    - forward() – Go to the next page.
    - quit() – Close the browser.
2. **WebElement**
- Represents HTML elements on a web page (like buttons, input fields, links).
- Provides methods to interact with elements:
    - click() – Click a button or link.
    - send_keys() – Enter text in input fields.
    - text – Get text of the element.
- Example:
```python
element = driver.find_element(By.ID, "username").send_keys("Raju")
```
3. **By**
- Used to local elements on a web page.
- Common strategies:
    - By.ID
    - By.NAME
    - By.XPATH
    - By.CSS_SELECTOR
- Example: 
```python
from selenium.webdriver.common.by import By  
element = driver.find_element(By.ID,"Username")
```
4. **WebdriverWait**
- Used for explicit waits to handle dynamic web elements.
- Waits until a condition is met or a timeout occurs.
- Example:
```python
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
wait = WebDriverWait(driver, 10)
element = wait.until(EC.visibility_of_element_located((By.ID, "username")))
```
5. **Actions**
- Used for advanced user interactions, like:
    - Mouse hover
    - Drag and drop
    - Double-click
    - Right-click
- Example:
```python
from selenium.webdriver import ActionChains
actions = ActionChains(driver)
actions.move_to_element(element).click().perform()
```