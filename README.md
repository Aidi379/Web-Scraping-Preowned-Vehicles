# Prior Knowledge

## HTTP Requests
HTTP (Hypertext Transfer Protocol) is the primary protocol used for transmitting web pages on the internet. When a user visits a webpage, their browser sends an HTTP request to the server hosting the site, and in response, the server sends back the requested page. There are several types of HTTP requests, but the two most relevant for web scraping are:

### GET
Requests data from a specified resource (e.g., a webpage). When you type a URL into your browser, a GET request is sent to the server to retrieve that page.
### POST 
Submits data to be processed to a specified resource, often leading to a change in the server's state or updates to the resource (e.g., submitting a form).
Understanding these requests is crucial because web scraping often involves programmatically sending these requests to retrieve data.

## HTML Format
HTML (Hypertext Markup Language) is the standard markup language used to create web pages. It structures the content on the web page using elements represented by tags. Basic understanding of the following HTML concepts is essential:

### Tags 
HTML documents are comprised of tags (e.g., `<html/>`, `<body/>`, `<div/>`, `<p/>`, `<a/>`), which define the type of content (paragraphs, links, images, etc.) and its structure on the page.
### Attributes
Tags can have attributes that provide additional information about an element (e.g., class, id, href). The class and id attributes are particularly important for web scraping, as they can be used to identify and select specific elements.
### DOM (Document Object Model)
The DOM represents the structure of an HTML document as a tree of objects. This is how browsers interpret HTML documents, and understanding it helps in navigating and selecting elements for scraping.

## CSS Selector
A CSS selector is a pattern used to select elements within an HTML document for styling purposes. In web scraping with BeautifulSoup, CSS selectors allow you to pinpoint elements based on various criteria such as tag names, classes, IDs, attributes, and their hierarchical relationships.

### Type Selector:
- Selects all elements of a given type.
- Example: div selects all <div> elements.

### Class Selector:
- Selects all elements with a specific class.
- Example: .class-name selects all elements with class="class-name".

### ID Selector:
- Selects the element with a specific ID.
- Example: #id-name selects the element with id="id-name".

## Connection Between HTTP Requests, HTML, CSS Selectors, and Web Scraping
When web scraping:
- An HTTP request (usually a GET request) is sent to the URL of the page you want to scrape.
- The server responds by sending back the HTML content of the page.
- The HTML content is then parsed and analyzed, often using libraries like BeautifulSoup, which allows you to navigate the DOM and extract information using tags, attributes, and CSS selectors.
- CSS selectors are used to pinpoint and select elements within the HTML document based on various criteria. This is where libraries like BeautifulSoup come into play, allowing us to use CSS selectors to find and extract the desired data from the HTML content.

# Project Intro
## Goal
As a car-renting platform, we would like to do data analysis of the current preowned vehicle market to
- Determine the price range and distribution of the cars on current second-hand market
- Use relevant information to determine the insurance policy and price the contracts

## Website we are scraping: Craigslist
Craigslist is a privately-held American company operating a classified advertisements website with sections devoted to jobs, housing, for sale, items wanted, services, community service, gigs, résumés, and discussion forums. And here today we would like to parse this website to get the price of pre-owned vehicles.

## Three Ways to Crawl Web Page Information
1. HTTP Requests: good for static pages, not apply to all websites, especially those dynamic with JavaScript.
2. Selenium: use selenium and chromedriver-autoinstaller for all websites, including dynamic ones. The only downside is that it runs slower.
3. API request: the simplest and fastest way. Only apply to those web pages use API end which is in Json format.
   
