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
      - 4**:  Client Error (your fault)
      - 5**:  Server Error
    - Status codes are followed by an action
      - HTML code to render the website
      - Code to render an error page
  - Request Headers
    - Contains additional information about a request/response
    - **Accept**:  Acceptable content-types for response (e.g. html,json, xml)
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

## Useful Modules

- **requests**:  A module that allows Python to access the request/response cycle of internet servers.

