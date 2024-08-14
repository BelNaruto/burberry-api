# Burberry API Documentation

This API provides endpoints to interact with Burberry's product catalog.

## Endpoints

### 1. Search Products

Searches for products based on a query string.

- **URL:** `/search`
- **Method:** GET
- **Query Parameters:**
  - `query` (required): The search term

#### Success Response

- **Code:** 200
- **Content:** JSON object containing search results

#### Error Responses

- **Code:** 400
  - **Content:** `{ "message": "Please provide the search" }`
- **Code:** 500
  - **Content:** `{ "message": "Error: [error message]" }`

### 2. Get Product Description

Retrieves the description of a specific product.

- **URL:** `/product-description`
- **Method:** GET
- **Query Parameters:**
  - `url` (required): The URL of the product

#### Success Response

- **Code:** 200
- **Content:** JSON object containing the product description

#### Error Responses

- **Code:** 400
  - **Content:** `{ "message": "Please provide the url" }`
- **Code:** 500
  - **Content:** `{ "message": "Error: [error message]" }`

### 3. Get Products by Category

Retrieves products belonging to a specific category.

- **URL:** `/products-by-category`
- **Method:** GET
- **Query Parameters:**
  - `categoryUrl` (required): The URL of the category

#### Success Response

- **Code:** 200
- **Content:** JSON object containing the products in the category

#### Error Responses

- **Code:** 400
  - **Content:** `{ "message": "Please provide the categoryUrl" }`
- **Code:** 500
  - **Content:** `{ "message": "Error: [error message]" }`

## Error Handling

All endpoints will return a 500 status code with an error message if an unexpected error occurs during processing.
