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




