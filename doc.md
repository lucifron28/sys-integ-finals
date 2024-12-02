# API Documentation

## Endpoints

### Books

#### Get All Books

- **URL:** `/api/books`
- **Method:** `GET`
- **Description:** Retrieve a list of all books.
- **Response (JSON):**
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
- **Response (XML):**
    ```xml
    <books>
        <book>
            <id>1</id>
            <title>Book Title</title>
            <author>Author Name</author>
            <published_date>YYYY-MM-DD</published_date>
        </book>
        ...
    </books>
    ```

#### Get Book by ID

- **URL:** `/api/books/{id}`
- **Method:** `GET`
- **Description:** Retrieve details of a specific book.
- **Response (JSON):**
    ```json
    {
        "id": 1,
        "title": "Book Title",
        "author": "Author Name",
        "published_date": "YYYY-MM-DD",
        "summary": "Book summary"
    }
    ```
- **Response (XML):**
    ```xml
    <book>
        <id>1</id>
        <title>Book Title</title>
        <author>Author Name</author>
        <published_date>YYYY-MM-DD</published_date>
        <summary>Book summary</summary>
    </book>
    ```

#### Add a New Book

- **URL:** `/api/books`
- **Method:** `POST`
- **Description:** Add a new book.
- **Request Body (JSON):**
    ```json
    {
        "title": "Book Title",
        "author": "Author Name",
        "published_date": "YYYY-MM-DD",
        "summary": "Book summary"
    }
    ```
- **Request Body (XML):**
    ```xml
    <book>
        <title>Book Title</title>
        <author>Author Name</author>
        <published_date>YYYY-MM-DD</published_date>
        <summary>Book summary</summary>
    </book>
    ```
- **Response (JSON):**
    ```json
    {
        "id": 1,
        "title": "Book Title",
        "author": "Author Name",
        "published_date": "YYYY-MM-DD",
        "summary": "Book summary"
    }
    ```
- **Response (XML):**
    ```xml
    <book>
        <id>1</id>
        <title>Book Title</title>
        <author>Author Name</author>
        <published_date>YYYY-MM-DD</published_date>
        <summary>Book summary</summary>
    </book>
    ```

#### Update Book by ID

- **URL:** `/api/books/{id}`
- **Method:** `PUT`
- **Description:** Update details of an existing book.
- **Request Body (JSON):**
    ```json
    {
        "title": "Updated Book Title",
        "author": "Updated Author Name",
        "published_date": "YYYY-MM-DD",
        "summary": "Updated book summary"
    }
    ```
- **Request Body (XML):**
    ```xml
    <book>
        <title>Updated Book Title</title>
        <author>Updated Author Name</author>
        <published_date>YYYY-MM-DD</published_date>
        <summary>Updated book summary</summary>
    </book>
    ```
- **Response (JSON):**
    ```json
    {
        "id": 1,
        "title": "Updated Book Title",
        "author": "Updated Author Name",
        "published_date": "YYYY-MM-DD",
        "summary": "Updated book summary"
    }
    ```
- **Response (XML):**
    ```xml
    <book>
        <id>1</id>
        <title>Updated Book Title</title>
        <author>Updated Author Name</author>
        <published_date>YYYY-MM-DD</published_date>
        <summary>Updated book summary</summary>
    </book>
    ```

#### Delete Book by ID

- **URL:** `/api/books/{id}`
- **Method:** `DELETE`
- **Description:** Delete a book.
- **Response (JSON):**
    ```json
    {
        "message": "Book deleted successfully"
    }
    ```
- **Response (XML):**
    ```xml
    <message>Book deleted successfully</message>
    ```

### Authors

#### Get All Authors

- **URL:** `/api/authors`
- **Method:** `GET`
- **Description:** Retrieve a list of all authors.
- **Response (JSON):**
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
- **Response (XML):**
    ```xml
    <authors>
        <author>
            <id>1</id>
            <name>Author Name</name>
            <birthdate>YYYY-MM-DD</birthdate>
        </author>
        ...
    </authors>
    ```

#### Get Author by ID

- **URL:** `/api/authors/{id}`
- **Method:** `GET`
- **Description:** Retrieve details of a specific author.
- **Response (JSON):**
    ```json
    {
        "id": 1,
        "name": "Author Name",
        "birthdate": "YYYY-MM-DD",
        "biography": "Author biography"
    }
    ```
- **Response (XML):**
    ```xml
    <author>
        <id>1</id>
        <name>Author Name</name>
        <birthdate>YYYY-MM-DD</birthdate>
        <biography>Author biography</biography>
    </author>
    ```

#### Add a New Author

- **URL:** `/api/authors`
- **Method:** `POST`
- **Description:** Add a new author.
- **Request Body (JSON):**
    ```json
    {
        "name": "Author Name",
        "birthdate": "YYYY-MM-DD",
        "biography": "Author biography"
    }
    ```
- **Request Body (XML):**
    ```xml
    <author>
        <name>Author Name</name>
        <birthdate>YYYY-MM-DD</birthdate>
        <biography>Author biography</biography>
    </author>
    ```
- **Response (JSON):**
    ```json
    {
        "id": 1,
        "name": "Author Name",
        "birthdate": "YYYY-MM-DD",
        "biography": "Author biography"
    }
    ```
- **Response (XML):**
    ```xml
    <author>
        <id>1</id>
        <name>Author Name</name>
        <birthdate>YYYY-MM-DD</birthdate>
        <biography>Author biography</biography>
    </author>
    ```

#### Update Author by ID

- **URL:** `/api/authors/{id}`
- **Method:** `PUT`
- **Description:** Update an author's information.
- **Request Body (JSON):**
    ```json
    {
        "name": "Updated Author Name",
        "birthdate": "YYYY-MM-DD",
        "biography": "Updated author biography"
    }
    ```
- **Request Body (XML):**
    ```xml
    <author>
        <name>Updated Author Name</name>
        <birthdate>YYYY-MM-DD</birthdate>
        <biography>Updated author biography</biography>
    </author>
    ```
- **Response (JSON):**
    ```json
    {
        "id": 1,
        "name": "Updated Author Name",
        "birthdate": "YYYY-MM-DD",
        "biography": "Updated author biography"
    }
    ```
- **Response (XML):**
    ```xml
    <author>
        <id>1</id>
        <name>Updated Author Name</name>
        <birthdate>YYYY-MM-DD</birthdate>
        <biography>Updated author biography</biography>
    </author>
    ```

#### Delete Author by ID

- **URL:** `/api/authors/{id}`
- **Method:** `DELETE`
- **Description:** Delete an author.
- **Response (JSON):**
    ```json
    {
        "message": "Author deleted successfully"
    }
    ```
- **Response (XML):**
    ```xml
    <message>Author deleted successfully</message>
    ```

### Actions

#### Borrow a Book

- **URL:** `/api/actions/borrow`
- **Method:** `POST`
- **Description:** Borrow a book.
- **Request Body (JSON):**
    ```json
    {
        "user_id": 1,
        "book_id": 1
    }
    ```
- **Request Body (XML):**
    ```xml
    <action>
        <user_id>1</user_id>
        <book_id>1</book_id>
    </action>
    ```
- **Response (JSON):**
    ```json
    {
        "message": "Book borrowed successfully",
        "borrowing_id": 1
    }
    ```
- **Response (XML):**
    ```xml
    <response>
        <message>Book borrowed successfully</message>
        <borrowing_id>1</borrowing_id>
    </response>
    ```

#### Return a Book

- **URL:** `/api/actions/return`
- **Method:** `POST`
- **Description:** Return a borrowed book.
- **Request Body (JSON):**
    ```json
    {
        "borrowing_id": 1
    }
    ```
- **Request Body (XML):**
    ```xml
    <action>
        <borrowing_id>1</borrowing_id>
    </action>
    ```
- **Response (JSON):**
    ```json
    {
        "message": "Book returned successfully"
    }
    ```
- **Response (XML):**
    ```xml
    <response>
        <message>Book returned successfully</message>
    </response>
    ```