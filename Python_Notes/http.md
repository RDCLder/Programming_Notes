# HTTP With Python

## Objectives

- Describe how URL works
- Describe the request/response cycle
- Explain a request or response header
- Explain the different categories of response codes
- Compare GET and POST requests

---

## General

- URL
  - Definition:  
  - Process
    1. DNS Lookup:  Finds the IP address of a URL (like a phonebook for the internet)
    2. Computer makes a REQUEST to a server
    3. Server processes the REQUEST
    4. Server issues a RESPONSE

- REQUEST/RESPONSE Cycle
  - The process through which a client obtains information from a server
  - Process
    - Client (e.g. computer) obtains an IP address and sends a REQUEST to the address
    - The corresponding server processes the REQUEST (e.g. access a database)
    - The server responds with a status code
      - 2xx:  Success
      - 3xx:  Redirect
      - 4xx:  Client Error (your fault)
      - 5xx:  Server Error
    - Status codes are followed by an action
      - HTML code to render the website
      - Code to render an error page
  - Request Headers
    - Contains additional information about a request/response
    - **Accept**:  Acceptable content-types for response (e.g. html, json, xml)
    - **Cache-Control**:  Specify caching behavior
    - **User-Agent**:  Information about the software used to make the request
  - Response Headers
    - **Access-Control-Allow-Origin**:  Specify domains that can make requests
    - **Allowed**:  HTTP verbs that are allowed in requests

- HTTP Verbs
  - Definition:  Actions that HTTP code can perform
  - **GET**:  Request for retrieving data.  Data passed in query string.  Should have no side effects.
  - **POST**:  Request for writing data.  Data passed in request body.  Can have side effects.

- API
  - Definition:  Application programming interface.  A set of clearly defined methods of communication among various components of computers.
    - Allows flow of information between applications without needing to understand how each application works.

## Requests Module

- **requests**:  A module that allows Python to access the request/response cycle of internet servers.
  - Uses
    - Make HTTP requests with Python
    - Web scrapping/crawling, grabbing data from other APIs, etc.

- Request Headers
  - A request for receiving output in a specific way.
    - e.g. Outputting in plain textor JSON instead of HTML
  - Syntax:  requests.get(URL, headers = {}, ) 
    - First argument is URL
    - Second optional argument is header which specifies requirements for the output
    - Headers is a dictionary.  Every key-value pair corresponds to a requirement and format required.
  - e.g.
  ```python
  import requests
  
  response = requests.get(
    "http://www.example.com",
    headers = {
      "Accept": "text/plain",
      "headers": "value2"
    }
  )
  ```

- Header Types
  - Accept:  Specifies the format to receive responses in
    - plain/text
    - application/json

- **.json()**:  A method that changes any output request in json format from a string to dictionary
  - More organized and easier to utilize than plain text.
  - e.g.
  ```python
  response = requests.get(url, headers = {'Accept': 'application/json'}
  data = response.json()
  ```

