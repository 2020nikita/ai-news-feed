# NewsAPI Documentation

## Overview
This documentation explains how to use the NewsAPI to fetch news articles for the AI-Powered Personalized News Feed project. The API provides access to thousands of news articles from various sources and categories.

## Getting an API Key
1. Go to the [NewsAPI website](https://newsapi.org/).
2. Sign up for a free account.
3. After signing up, you’ll receive an API key.
4. Use this key to authenticate your requests.

## API Endpoints

### 1. Top Headlines
Fetches the latest news articles.

**URL:https://newsapi.org/v2/top-headlines**


**Parameters:**
- `country`: The country code (e.g., `us` for the United States).
- `apiKey`: Your API key.

**Example Request:GET https://newsapi.org/v2/top-headlines?country=us&apiKey=YOUR_API_KEY**


### 2. Everything
Searches for news articles by keyword.

**URL:https://newsapi.org/v2/everything**


**Parameters:**
- `q`: The search keyword (e.g., `technology`).
- `apiKey`: Your API key.

**Example Request:GET https://newsapi.org/v2/everything?q=technology&apiKey=YOUR_API_KEY**

## Example Responses

### Top Headlines Response
```json
{
  "status": "ok",
  "totalResults": 10,
  "articles": [
    {
      "title": "Example News Title",
      "description": "This is an example news description.",
      "url": "https://example.com/news",
      "urlToImage": "https://example.com/image.jpg",
      "publishedAt": "2023-10-01T12:00:00Z"
    }
  ]
}

{
  "status": "ok",
  "totalResults": 5,
  "articles": [
    {
      "title": "Example Search Result",
      "description": "This is an example search result.",
      "url": "https://example.com/search-result",
      "urlToImage": "https://example.com/search-image.jpg",
      "publishedAt": "2023-10-01T12:00:00Z"
    }
  ]
}


---

#### **Step 6: Add Code Examples**
Include code snippets showing how to use the API in your project. For example, how to fetch news in Python.

```markdown
## Code Examples

### Fetching Top Headlines in Python
```python
import requests

# API endpoint and parameters
url = "https://newsapi.org/v2/top-headlines"
params = {
    "country": "us",
    "apiKey": "YOUR_API_KEY"
}

# Make the request
response = requests.get(url, params=params)
data = response.json()

# Print the news articles
for article in data["articles"]:
    print(article["title"])
    print(article["description"])
    print("-----")

    
---

