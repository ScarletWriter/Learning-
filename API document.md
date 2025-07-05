# API Documentation: Open Library API Integration  

## Overview  

This documentation explains how to integrate with the Open Library API to fetch book details, search for books, and retrieve author information. This is a simplified version of the actual Open Library API, adapted for demonstration. 

## Base URL  

All endpoints start with:  

``
https://openlibrary.org  
``   
## Authentication
The Open Library API is public and does not require authentication.  
## Rate Limits  
- 100 requests/minute per IP address.
- Exceeding limits returns a 429 Too Many Requests status.
## Endpoints  
### GET /search.json  
*Search for books by title, author, or ISBN.*  
### Query Parameters  

| Parameter	                       | Type	                   | Description                                |
|----------------------------------|-------------------------|--------------------------------------------|
|     q                            |  string                 | 	Search query (required)                   |
| page                             | int                     | Page number (default: 1)                   |
| limit                            | int                     | Results per page (default: 10, max: 100)   |  

## Example Request
``
curl -X GET "https://openlibrary.org/search.json?q=harry+potter&limit=2"
``  
## Example Response  
```````````
{  
  "numFound": 215,  
  "start": 0,  
  "docs": [  
    {  
      "title": "Harry Potter and the Philosopher's Stone",  
      "author_name": ["J.K. Rowling"],  
      "isbn": ["978-0439708180"],  
      "first_publish_year": 1997  
    },  
    {  
      "title": "Harry Potter and the Chamber of Secrets",  
      "author_name": ["J.K. Rowling"],  
      "isbn": ["978-0439064873"],  
      "first_publish_year": 1998  
    }  
  ]  
}
  ```````````  

## **GET /works/{work_id}.json**





