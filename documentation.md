# Library Book Management API Documentation

## Overview
The Library Book Management API allows users to manage books in a library. It provides endpoints to create, read, update, and delete books. The API follows RESTful principles and meets level 2 of the Richardson REST API maturity model.

## Base URL
```
https://api.librarymanagement.com/v1
```

## Endpoints

### Get All Books
```
GET /books
```
**Description:** Retrieve a list of all books in the library.

**Response:**
- `200 OK`: Returns a JSON or XML array of books.

**Example (JSON):**
```json
[
    {
        "id": 1,
        "title": "The Great Gatsby",
        "author": "F. Scott Fitzgerald",
        "isbn": "9780743273565",
        "publishedDate": "1925-04-10"
    },
    ...
]
```

**Example (XML):**
```xml
<books>
    <book>
        <id>1</id>
        <title>The Great Gatsby</title>
        <author>F. Scott Fitzgerald</author>
        <isbn>9780743273565</isbn>
        <publishedDate>1925-04-10</publishedDate>
    </book>
    ...
</books>
```

### Get a Book by ID
```
GET /books/{id}
```
**Description:** Retrieve a specific book by its ID.

**Path Parameters:**
- `id` (integer): The ID of the book.

**Response:**
- `200 OK`: Returns the book details in JSON or XML.
- `404 Not Found`: Book not found.

**Example (JSON):**
```json
{
    "id": 1,
    "title": "The Great Gatsby",
    "author": "F. Scott Fitzgerald",
    "isbn": "9780743273565",
    "publishedDate": "1925-04-10"
}
```

**Example (XML):**
```xml
<book>
    <id>1</id>
    <title>The Great Gatsby</title>
    <author>F. Scott Fitzgerald</author>
    <isbn>9780743273565</isbn>
    <publishedDate>1925-04-10</publishedDate>
</book>
```

### Create a New Book
```
POST /books
```
**Description:** Add a new book to the library.

**Request Body:**
- `title` (string): The title of the book.
- `author` (string): The author of the book.
- `isbn` (string): The ISBN of the book.
- `publishedDate` (string): The published date of the book.

**Response:**
- `201 Created`: Returns the created book details in JSON or XML.

**Example (JSON):**
```json
{
    "title": "1984",
    "author": "George Orwell",
    "isbn": "9780451524935",
    "publishedDate": "1949-06-08"
}
```

**Example (XML):**
```xml
<book>
    <title>1984</title>
    <author>George Orwell</author>
    <isbn>9780451524935</isbn>
    <publishedDate>1949-06-08</publishedDate>
</book>
```

### Update a Book
```
PUT /books/{id}
```
**Description:** Update the details of an existing book.

**Path Parameters:**
- `id` (integer): The ID of the book.

**Request Body:**
- `title` (string): The title of the book.
- `author` (string): The author of the book.
- `isbn` (string): The ISBN of the book.
- `publishedDate` (string): The published date of the book.

**Response:**
- `200 OK`: Returns the updated book details in JSON or XML.
- `404 Not Found`: Book not found.

**Example (JSON):**
```json
{
    "title": "1984",
    "author": "George Orwell",
    "isbn": "9780451524935",
    "publishedDate": "1949-06-08"
}
```

**Example (XML):**
```xml
<book>
    <title>1984</title>
    <author>George Orwell</author>
    <isbn>9780451524935</isbn>
    <publishedDate>1949-06-08</publishedDate>
</book>
```

### Delete a Book
```
DELETE /books/{id}
```
**Description:** Delete a book from the library.

**Path Parameters:**
- `id` (integer): The ID of the book.

**Response:**
- `204 No Content`: Book successfully deleted.
- `404 Not Found`: Book not found.

### Get All Authors
```
GET /authors
```
**Description:** Retrieve a list of all authors in the library.

**Response:**
- `200 OK`: Returns a JSON or XML array of authors.

**Example (JSON):**
```json
[
    {
        "id": 1,
        "name": "F. Scott Fitzgerald",
        "birthdate": "1896-09-24"
    },
    ...
]
```

**Example (XML):**
```xml
<authors>
    <author>
        <id>1</id>
        <name>F. Scott Fitzgerald</name>
        <birthdate>1896-09-24</birthdate>
    </author>
    ...
</authors>
```

### Get an Author by ID
```
GET /authors/{id}
```
**Description:** Retrieve a specific author by their ID.

**Path Parameters:**
- `id` (integer): The ID of the author.

**Response:**
- `200 OK`: Returns the author details in JSON or XML.
- `404 Not Found`: Author not found.

**Example (JSON):**
```json
{
    "id": 1,
    "name": "F. Scott Fitzgerald",
    "birthdate": "1896-09-24"
}
```

**Example (XML):**
```xml
<author>
    <id>1</id>
    <name>F. Scott Fitzgerald</name>
    <birthdate>1896-09-24</birthdate>
</author>
```

### Create a New Author
```
POST /authors
```
**Description:** Add a new author to the library.

**Request Body:**
- `name` (string): The name of the author.
- `birthdate` (string): The birthdate of the author.

**Response:**
- `201 Created`: Returns the created author details in JSON or XML.

**Example (JSON):**
```json
{
    "name": "George Orwell",
    "birthdate": "1903-06-25"
}
```

**Example (XML):**
```xml
<author>
    <name>George Orwell</name>
    <birthdate>1903-06-25</birthdate>
</author>
```

### Update an Author
```
PUT /authors/{id}
```
**Description:** Update the details of an existing author.

**Path Parameters:**
- `id` (integer): The ID of the author.

**Request Body:**
- `name` (string): The name of the author.
- `birthdate` (string): The birthdate of the author.

**Response:**
- `200 OK`: Returns the updated author details in JSON or XML.
- `404 Not Found`: Author not found.

**Example (JSON):**
```json
{
    "name": "George Orwell",
    "birthdate": "1903-06-25"
}
```

**Example (XML):**
```xml
<author>
    <name>George Orwell</name>
    <birthdate>1903-06-25</birthdate>
</author>
```

### Delete an Author
```
DELETE /authors/{id}
```
**Description:** Delete an author from the library.

**Path Parameters:**
- `id` (integer): The ID of the author.

**Response:**
- `204 No Content`: Author successfully deleted.
- `404 Not Found`: Author not found.

## Error Handling
The API uses standard HTTP status codes to indicate the success or failure of an API request. Common status codes include:
- `200 OK`: The request was successful.
- `201 Created`: The resource was successfully created.
- `204 No Content`: The resource was successfully deleted.
- `400 Bad Request`: The request was invalid or cannot be served.
- `404 Not Found`: The requested resource could not be found.
- `500 Internal Server Error`: An error occurred on the server.

## Authentication
The API uses token-based authentication. Include the token in the `Authorization` header of each request:
```
Authorization: Bearer {token}
```

## Rate Limiting
The API enforces rate limiting to ensure fair usage. The rate limit is 100 requests per minute. If the limit is exceeded, a `429 Too Many Requests` response will be returned.

## Contact
For any questions or support, please contact support@librarymanagement.com.
