# API Documentation

## Endpoints

### Books

#### Get All Books

- **URL:** `/api/books`
- **Method:** `GET`
- **Description:** Retrieve a list of all books.
- **Response:**
    ```json
    [
        {
            "id": 1,
            "title": "Book Title",
            "author": "Author Name",
            "published_date": "YYYY-MM-DD"
        },
        ...
    ]
    ```

#### Get Book by ID

- **URL:** `/api/books/{id}`
- **Method:** `GET`
- **Description:** Retrieve details of a specific book.
- **Response:**
    ```json
    {
        "id": 1,
        "title": "Book Title",
        "author": "Author Name",
        "published_date": "YYYY-MM-DD",
        "summary": "Book summary"
    }
    ```

#### Add a New Book

- **URL:** `/api/books`
- **Method:** `POST`
- **Description:** Add a new book.
- **Request Body:**
    ```json
    {
        "title": "Book Title",
        "author": "Author Name",
        "published_date": "YYYY-MM-DD",
        "summary": "Book summary"
    }
    ```
- **Response:**
    ```json
    {
        "id": 1,
        "title": "Book Title",
        "author": "Author Name",
        "published_date": "YYYY-MM-DD",
        "summary": "Book summary"
    }
    ```

#### Update Book by ID

- **URL:** `/api/books/{id}`
- **Method:** `PUT`
- **Description:** Update details of an existing book.
- **Request Body:**
    ```json
    {
        "title": "Updated Book Title",
        "author": "Updated Author Name",
        "published_date": "YYYY-MM-DD",
        "summary": "Updated book summary"
    }
    ```
- **Response:**
    ```json
    {
        "id": 1,
        "title": "Updated Book Title",
        "author": "Updated Author Name",
        "published_date": "YYYY-MM-DD",
        "summary": "Updated book summary"
    }
    ```

#### Delete Book by ID

- **URL:** `/api/books/{id}`
- **Method:** `DELETE`
- **Description:** Delete a book.
- **Response:**
    ```json
    {
        "message": "Book deleted successfully"
    }
    ```

### Authors

#### Get All Authors

- **URL:** `/api/authors`
- **Method:** `GET`
- **Description:** Retrieve a list of all authors.
- **Response:**
    ```json
    [
        {
            "id": 1,
            "name": "Author Name",
            "birthdate": "YYYY-MM-DD"
        },
        ...
    ]
    ```

#### Get Author by ID

- **URL:** `/api/authors/{id}`
- **Method:** `GET`
- **Description:** Retrieve details of a specific author.
- **Response:**
    ```json
    {
        "id": 1,
        "name": "Author Name",
        "birthdate": "YYYY-MM-DD",
        "biography": "Author biography"
    }
    ```

#### Add a New Author

- **URL:** `/api/authors`
- **Method:** `POST`
- **Description:** Add a new author.
- **Request Body:**
    ```json
    {
        "name": "Author Name",
        "birthdate": "YYYY-MM-DD",
        "biography": "Author biography"
    }
    ```
- **Response:**
    ```json
    {
        "id": 1,
        "name": "Author Name",
        "birthdate": "YYYY-MM-DD",
        "biography": "Author biography"
    }
    ```

#### Update Author by ID

- **URL:** `/api/authors/{id}`
- **Method:** `PUT`
- **Description:** Update an author's information.
- **Request Body:**
    ```json
    {
        "name": "Updated Author Name",
        "birthdate": "YYYY-MM-DD",
        "biography": "Updated author biography"
    }
    ```
- **Response:**
    ```json
    {
        "id": 1,
        "name": "Updated Author Name",
        "birthdate": "YYYY-MM-DD",
        "biography": "Updated author biography"
    }
    ```

#### Delete Author by ID

- **URL:** `/api/authors/{id}`
- **Method:** `DELETE`
- **Description:** Delete an author.
- **Response:**
    ```json
    {
        "message": "Author deleted successfully"
    }
    ```

### Actions

#### Borrow a Book

- **URL:** `/api/actions/borrow`
- **Method:** `POST`
- **Description:** Borrow a book.
- **Request Body:**
    ```json
    {
        "user_id": 1,
        "book_id": 1
    }
    ```
- **Response:**
    ```json
    {
        "message": "Book borrowed successfully",
        "borrowing_id": 1
    }
    ```

#### Return a Book

- **URL:** `/api/actions/return`
- **Method:** `POST`
- **Description:** Return a borrowed book.
- **Request Body:**
    ```json
    {
        "borrowing_id": 1
    }
    ```
- **Response:**
    ```json
    {
        "message": "Book returned successfully"
    }
    ```