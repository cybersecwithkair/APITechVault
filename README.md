# APITechVault

# TechVault API

## Overview
TechVault API is a powerful and secure API designed to fetch technical documentation from various sources, specifically MDN Web Docs, and generate concise summaries. This API simplifies access to large documentation files, providing users with key insights quickly and efficiently.

## Features
- **Fetch MDN Documentation**: Retrieve documentation from MDN Web Docs for a given web technology topic.
- **Summarization**: Extract and display concise content for easy understanding.
- **Secure Access**: Implemented API security measures to prevent unauthorized access.
- **Postman Testing**: Fully tested and validated using Postman.

## Technology Stack
- **Backend**: Python
- **Framework**: FastAPI
- **Web Scraping**: BeautifulSoup
- **Security Measures**: Input validation, request headers, and error handling

## Installation

### Prerequisites
Ensure you have the following installed on your system:
- Python 3.x
- Postman (for testing)

### Steps to Install
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/techvault-api.git
   cd techvault-api
   ```
2. Install dependencies:
   ```bash
   pip install fastapi uvicorn beautifulsoup4 requests
   ```
3. Start the server:
   ```bash
   uvicorn main:app --reload
   ```

## API Endpoints

### Home Route
**GET /**
- Description: Returns a welcome message.
- Request Example:
  ```bash
  curl -X GET "http://127.0.0.1:8000/"
  ```
- Response:
  ```json
  {
    "message": "Welcome to TechVault API"
  }
  ```

### Fetch MDN Documentation
**GET /mdn/{topic}**
- Description: Fetches documentation from MDN Web Docs for a specified topic.
- Request Example:
  ```bash
  curl -X GET "http://127.0.0.1:8000/mdn/HTML"
  ```
- Response:
  ```json
  {
    "title": "HTML",
    "url": "https://developer.mozilla.org/en-US/docs/Web/HTML",
    "content": "Brief content extracted from MDN documentation..."
  }
  ```

## Security Measures
To ensure security, the following measures have been implemented:
- **User-Agent Header**: Prevents being blocked by MDN Web Docs.
- **Error Handling**: Returns appropriate messages if documentation is unavailable.
- **Input Validation**: Ensures only valid web technologies are queried.

## Testing with Postman
1. Open Postman and enter the API URL (`http://127.0.0.1:8000/mdn/{topic}`).
2. Send a GET request to fetch documentation.
3. Validate the response to ensure accurate data retrieval.

## Future Enhancements
- Support for additional documentation sources.
- AI-powered summarization for better insights.
- Web UI to interact with the API visually.



