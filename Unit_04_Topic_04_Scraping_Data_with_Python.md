---
title: "Unit IV: Scraping Data from a Website using Python"
id: unit4-topic4-scraping-with-python
tags:
  - unit-4
  - web-scraping
  - python
  - requests
  - beautifulsoup
aliases:
  - "Python Web Scraping"
links:
  - "[[UITx/Unit_04_Topic_03_Python_Setup_for_Scraping.md|Python Setup for Scraping]]"
  - "[[UITx/Unit_04_Topic_05_Intro_to_Human_Computer_Interaction.md|Introduction to Human-Computer Interaction]]"
---

# Unit IV, Topic 4: Scraping Data from a Website using Python

> [!quote] With our workshop prepared, we can now begin the practical craft of web scraping. Using Python's powerful libraries, we will learn to request a web page, parse its HTML structure, and extract the specific data we seek. This is where theory meets practice, transforming raw web content into structured, valuable information.

## 1. The Core Libraries: `requests` and `BeautifulSoup`

For scraping static websites (where content is present in the initial HTML and not loaded by JavaScript), the combination of `requests` and `BeautifulSoup` is the standard and most effective approach.

-   **`requests`**: Fetches the web page.
-   **`BeautifulSoup`**: Parses the fetched HTML and helps us navigate and search it.

## 2. Step-by-Step Scraping Process

Let's walk through a complete example of scraping data from a simple, fictional website.

**Goal:** Scrape the titles and prices of products from a website.

**Example HTML (`products.html`):**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Our Products</title>
</head>
<body>
    <h1>Product List</h1>
    <div class="product-card">
        <h2 class="product-title">Laptop</h2>
        <p>A high-performance laptop.</p>
        <span class="price">$1200</span>
    </div>
    <div class="product-card">
        <h2 class="product-title">Mouse</h2>
        <p>An ergonomic wireless mouse.</p>
        <span class="price">$25</span>
    </div>
    <div class="product-card">
        <h2 class="product-title">Keyboard</h2>
        <p>A mechanical keyboard.</p>
        <span class="price">$75</span>
    </div>
</body>
</html>
```

### Step 1: Make an HTTP Request
First, we use the `requests` library to send a GET request to the URL and get the page's HTML content.

```python
import requests

# The URL of the website we want to scrape
URL = "http://example.com/products.html" # Replace with a real URL for a live test

# Send the HTTP GET request
try:
    response = requests.get(URL)
    # Raise an exception for bad status codes (4xx or 5xx)
    response.raise_for_status() 
    
    # Get the HTML content of the page
    html_content = response.text
    print("Successfully fetched the page.")

except requests.exceptions.RequestException as e:
    print(f"Error fetching the URL: {e}")
    exit()
```
-   `response.raise_for_status()`: This is a good practice to check if the request was successful (i.e., status code 200).

### Step 2: Parse the HTML with BeautifulSoup
Next, we create a `BeautifulSoup` object to parse the HTML content.

```python
from bs4 import BeautifulSoup

# Create a BeautifulSoup object
# 'lxml' is a fast and efficient parser
soup = BeautifulSoup(html_content, 'lxml')
```

### Step 3: Find and Extract the Data
Now we can use BeautifulSoup's methods to find the elements we need.

-   **`find(tag, class_)`**: Finds the *first* element that matches the criteria.
-   **`find_all(tag, class_)`**: Finds *all* elements that match the criteria and returns them as a list.

We want to find all the product cards, which are `<div>` elements with the class `product-card`.

```python
# Find all product cards
product_cards = soup.find_all('div', class_='product-card')

# A list to store our extracted data
scraped_data = []

# Loop through each product card to extract its details
for card in product_cards:
    # Find the title within the card
    title_element = card.find('h2', class_='product-title')
    title = title_element.text.strip() if title_element else "N/A"

    # Find the price within the card
    price_element = card.find('span', class_='price')
    price = price_element.text.strip() if price_element else "N/A"

    # Store the extracted data
    scraped_data.append({
        "title": title,
        "price": price
    })

print(scraped_data)
```
-   `.text`: Gets the text content of an element.
-   `.strip()`: Removes any leading/trailing whitespace.
-   We check if `title_element` and `price_element` exist before trying to access `.text` to avoid errors if a card is missing some information.

### Step 4: Store the Data (e.g., in a CSV file)
Finally, we can save our structured data into a file. A CSV (Comma-Separated Values) file is a common choice.

```python
import csv

# Define the CSV file name
filename = 'products.csv'

# Define the headers for the CSV file
headers = ['title', 'price']

# Write the data to the CSV file
try:
    with open(filename, 'w', newline='', encoding='utf-8') as csvfile:
        writer = csv.DictWriter(csvfile, fieldnames=headers)
        
        # Write the header row
        writer.writeheader()
        
        # Write the data rows
        writer.writerows(scraped_data)
    
    print(f"Data successfully saved to {filename}")

except IOError:
    print("I/O error")
```

## 4. Complete Script

Putting it all together:

```python
import requests
from bs4 import BeautifulSoup
import csv

URL = "http://example.com/products.html" # Replace with a real URL

try:
    response = requests.get(URL)
    response.raise_for_status()
    
    soup = BeautifulSoup(response.text, 'lxml')
    
    product_cards = soup.find_all('div', class_='product-card')
    scraped_data = []

    for card in product_cards:
        title = card.find('h2', class_='product-title').text.strip()
        price = card.find('span', class_='price').text.strip()
        scraped_data.append({"title": title, "price": price})

    with open('products.csv', 'w', newline='', encoding='utf-8') as f:
        writer = csv.DictWriter(f, fieldnames=['title', 'price'])
        writer.writeheader()
        writer.writerows(scraped_data)
        
    print("Scraping complete. Data saved to products.csv")

except requests.exceptions.RequestException as e:
    print(f"Error fetching URL: {e}")
except IOError:
    print("Error writing to file.")
except AttributeError:
    print("Error parsing the page. Check if the HTML structure has changed.")
```

## 5. Exam-Oriented Insights

The practical application of scraping libraries is a key topic.

> [!question] **Potential 2-Mark Questions:**
> 1.  **What is the role of the `requests` library in a Python web scraping script?**
>     *Answer:* The `requests` library is used to send HTTP requests (typically GET requests) to a URL to fetch the raw HTML content of the web page.
> 2.  **What is the role of the `BeautifulSoup` library?**
>     *Answer:* `BeautifulSoup` is used to parse the raw HTML content fetched by `requests`. It creates a parse tree that allows for easy navigation and extraction of data from the HTML structure.
> 3.  **What is the difference between `find()` and `find_all()` in BeautifulSoup?**
>     *Answer:* `find()` returns only the first element that matches a given criteria, while `find_all()` returns a list of all elements that match the criteria.
> 4.  **Why is it important to handle exceptions in a web scraping script?**
>     *Answer:* To make the script robust against issues like network errors (e.g., the website is down), HTTP errors (e.g., page not found), or changes in the website's HTML structure that could cause parsing errors.

> [!tip] **For Higher Mark Questions:**
> Be prepared to write a complete Python script that scrapes specific information (e.g., headlines from a news site, product names from an e-commerce page) from a provided HTML snippet. Explain each step of the process: making the request, parsing the HTML, finding the relevant elements using tags and classes, extracting the text, and storing the data. Discuss how you would modify your approach if the target website loaded its data using JavaScript.
