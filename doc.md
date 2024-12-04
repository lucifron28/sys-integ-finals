<div align="center" style="font-size: 30px;"><strong>Library Management System</strong></div>
<div align="center" style="font-size: 30px;"><strong>API Documentation</strong></div>

## Endpoints

### Books

#### Get All Books

- **URL:** `/api/book`
- **Method:** `GET`
- **Description:** Retrieve a list of all books.
- **Headers:**
  - Accept: application/json, application/xml
- **Response (JSON):**
    ```json
    [
        {
            "id": 1, // integer
            "title": "Pride and Prejudice", // string
            "author": "Jane Austen", // string
            "publishedDate": "1813-01-28", // string (date, YYYY-MM-DD)
            "genre": "Romance" // string
        },
        {
            "id": 2,
            "title": "I hope this doesn't find you",
            "author": "Ann Liang",
            "publishedDate": "2022-05-10",
            "genre": "Young Adult"
        },
        {
            "id": 3,
            "title": "1984",
            "author": "George Orwell",
            "publishedDate": "1949-06-08",
            "genre": "Dystopian"
        },
        {
            "id": 4,
            "title": "To Kill a Mockingbird",
            "author": "Harper Lee",
            "publishedDate": "1960-07-11",
            "genre": "Fiction"
        }
    ]
    ```
- **Response (XML):**
    ```xml
    <book>
        <book>
            <id>1</id> <!-- integer -->
            <title>Pride and Prejudice</title> <!-- string -->
            <author>Jane Austen</author> <!-- string -->
            <publishedDate>1813-01-28</publishedDate> <!-- string (date, YYYY-MM-DD) -->
            <genre>Romance</genre> <!-- string -->
        </book>
        <book>
            <id>2</id>
            <title>I hope this doesn't find you</title>
            <author>Ann Liang</author>
            <publishedDate>2022-05-10</publishedDate>
            <genre>Young Adult</genre>
        </book>
        <book>
            <id>3</id>
            <title>1984</title>
            <author>George Orwell</author>
            <publishedDate>1949-06-08</publishedDate>
            <genre>Dystopian</genre>
        </book>
        <book>
            <id>4</id>
            <title>To Kill a Mockingbird</title>
            <author>Harper Lee</author>
            <publishedDate>1960-07-11</publishedDate>
            <genre>Fiction</genre>
        </book>
    </book>
    ```

- **Query Parameters:**
  - `title` (optional, string): Filter books by title.
  - `author` (optional, string): Filter books by author.
  - `genre` (optional, string): Filter books by genre.
  - `publishedDate` (optional, string, date, YYYY-MM-DD): Filter books by published date.
- **Example Request:**
  - `/api/book?author=George%20Orwell&genre=Dystopian`
- **Response (JSON):**
    ```json
    [
        {
            "id": 3,
            "title": "1984",
            "author": "George Orwell",
            "publishedDate": "1949-06-08",
            "summary": "A dystopian social science fiction novel and cautionary tale about the dangers of totalitarianism.",
            "genre": "Dystopian"
        },
        {
            "id": 6,
            "title": "Animal Farm",
            "author": "George Orwell",
            "publishedDate": "1945-08-17",
            "summary": "A satirical allegorical novella that criticizes the Russian Revolution and the Soviet Union.",
            "genre": "Dystopian"
        }
    ]
    ```
- **Response: (XML)**
    ```xml
    <book>
        <book>
            <id>3</id>
            <title>1984</title>
            <author>George Orwell</author>
            <publishedDate>1949-06-08</publishedDate>
            <summary>A dystopian social science fiction novel and cautionary tale about the dangers of totalitarianism.</summary>
            <genre>Dystopian</genre>
        </book>
        <book>
            <id>4</id>
            <title>Animal Farm</title>
            <author>George Orwell</author>
            <publishedDate>1945-08-17</publishedDate>
            <summary>A satirical allegorical novella that criticizes the Russian Revolution and the Soviet Union.</summary>
            <genre>Dystopian</genre>
        </book>
    </book>
    ```

#### Get Book by ID

- **URL:** `/api/book/{id}`
- **Method:** `GET`
- **Description:** Retrieve details of a specific book.
- **Headers:**
  - Accept: application/json, application/xml
- **Response (JSON):**
    ```json
    {
        "id": 1, // integer
        "title": "1984", // string
        "author": "George Orwell", // string
        "publishedDate": "1949-06-08", // string (date, YYYY-MM-DD)
        "summary": "A dystopian social science fiction novel and cautionary tale about the dangers of totalitarianism.", // string
        "genre": "Dystopian" // string
    }
    ```
- **Response (XML):**
    ```xml
    <book>
        <id>1</id> <!-- integer -->
        <title>1984</title> <!-- string -->
        <author>George Orwell</author> <!-- string -->
        <publishedDate>1949-06-08</publishedDate> <!-- string (date, YYYY-MM-DD) -->
        <summary>A dystopian social science fiction novel and cautionary tale about the dangers of totalitarianism.</summary> <!-- string -->
        <genre>Dystopian</genre> <!-- string -->
    </book>
    ```

#### Add a New Book

- **URL:** `/api/book`
- **Method:** `POST`
- **Description:** Add a new book.
- **Headers:**
  - Content-Type: application/json, application/xml
- **Request Body (JSON):**
    ```json
    {
        "title": "Brave New World", // string
        "author": "Aldous Huxley", // string
        "publishedDate": "1932-08-30", // string (date, YYYY-MM-DD)
        "summary": "A dystopian social science fiction novel set in a futuristic World State.", // string
        "genre": "Dystopian" // string
    }
    ```
- **Request Body (XML):**
    ```xml
    <book>
        <title>Brave New World</title> <!-- string -->
        <author>Aldous Huxley</author> <!-- string -->
        <publishedDate>1932-08-30</publishedDate> <!-- string (date, YYYY-MM-DD) -->
        <summary>A dystopian social science fiction novel set in a futuristic World State.</summary> <!-- string -->
        <genre>Dystopian</genre> <!-- string -->
    </book>
    ```
- **Response (JSON):**
    ```json
    {
        "id": 5, // integer
        "title": "Brave New World", // string
        "author": "Aldous Huxley", // string
        "publishedDate": "1932-08-30", // string (date, YYYY-MM-DD)
        "summary": "A dystopian social science fiction novel set in a futuristic World State.", // string
        "genre": "Dystopian" // string
    }
    ```
- **Response (XML):**
    ```xml
    <book>
        <id>5</id> <!-- integer -->
        <title>Brave New World</title> <!-- string -->
        <author>Aldous Huxley</author> <!-- string -->
        <publishedDate>1932-08-30</publishedDate> <!-- string (date, YYYY-MM-DD) -->
        <summary>A dystopian social science fiction novel set in a futuristic World State.</summary> <!-- string -->
        <genre>Dystopian</genre> <!-- string -->
    </book>
    ```

#### Update Book by ID

- **URL:** `/api/book/{id}`
- **Method:** `PUT`
- **Description:** Update details of an existing book.
- **Headers:**
  - Content-Type: application/json, application/xml
- **Request Body (JSON):**
    ```json
    {
        "title": "Animal Farm", // string
        "author": "George Orwell", // string
        "publishedDate": "1945-08-17", // string (date, YYYY-MM-DD)
        "summary": "A satirical allegorical novella reflecting events leading up to the Russian Revolution of 1917.", // string
        "genre": "Political Satire" // string
    }
    ```
- **Request Body (XML):**
    ```xml
    <book>
        <title>Animal Farm</title> <!-- string -->
        <author>George Orwell</author> <!-- string -->
        <publishedDate>1945-08-17</publishedDate> <!-- string (date, YYYY-MM-DD) -->
        <summary>A satirical allegorical novella reflecting events leading up to the Russian Revolution of 1917.</summary> <!-- string -->
        <genre>Political Satire</genre> <!-- string -->
    </book>
    ```
- **Response (JSON):**
    ```json
    {
        "id": 6, // integer
        "title": "Animal Farm", // string
        "author": "George Orwell", // string
        "publishedDate": "1945-08-17", // string (date, YYYY-MM-DD)
        "summary": "A satirical allegorical novella reflecting events leading up to the Russian Revolution of 1917.", // string
        "genre": "Political Satire" // string
    }
    ```
- **Response (XML):**
    ```xml
    <book>
        <id>6</id> <!-- integer -->
        <title>Animal Farm</title> <!-- string -->
        <author>George Orwell</author> <!-- string -->
        <publishedDate>1945-08-17</publishedDate> <!-- string (date, YYYY-MM-DD) -->
        <summary>A satirical allegorical novella reflecting events leading up to the Russian Revolution of 1917.</summary> <!-- string -->
        <genre>Political Satire</genre> <!-- string -->
    </book>
    ```

#### Delete Book by ID

- **URL:** `/api/book/{id}`
- **Method:** `DELETE`
- **Description:** Delete a book.
- **Headers:**
  - Accept: application/json, application/xml
- **Response (JSON):**
    ```json
    {
        "message": "Book deleted successfully" // string
    }
    ```
- **Response (XML):**
    ```xml
    <message>Book deleted successfully</message> <!-- string -->
    ```

### Authors

#### Get All Authors

- **URL:** `/api/book/author`
- **Method:** `GET`
- **Description:** Retrieve a list of all authors.
- **Headers:**
  - Accept: application/json, application/xml
- **Response (JSON):**
    ```json
    [
        {
            "id": 1, // integer
            "name": "Jane Austen", // string
            "birthdate": "1775-12-16" // string (date, YYYY-MM-DD)
        },
        {
            "id": 2,
            "name": "George Orwell",
            "birthdate": "1903-06-25"
        },
        {
            "id": 3,
            "name": "Harper Lee",
            "birthdate": "1926-04-28"
        },
        {
            "id": 4,
            "name": "Ann Liang",
            "birthdate": "1995-08-15"
        },
        {
            "id": 5,
            "name": "Aldous Huxley",
            "birthdate": "1894-07-26"
        }
    ]
    ```
- **Response (XML):**
    ```xml
    <author>
        <author>
            <id>1</id> <!-- integer -->
            <name>Jane Austen</name> <!-- string -->
            <birthdate>1775-12-16</birthdate> <!-- string (date, YYYY-MM-DD) -->
        </author>
        <author>
            <id>2</id>
            <name>George Orwell</name>
            <birthdate>1903-06-25</birthdate>
        </author>
        <author>
            <id>3</id>
            <name>Harper Lee</name>
            <birthdate>1926-04-28</birthdate>
        </author>
        <author>
            <id>4</id>
            <name>Ann Liang</name>
            <birthdate>1995-08-15</birthdate>
        </author>
        <author>
            <id>5</id>
            <name>Aldous Huxley</name>
            <birthdate>1894-07-26</birthdate>
        </author>
    </author>
    ```

#### Get Author by ID

- **URL:** `/api/book/author/{id}`
- **Method:** `GET`
- **Description:** Retrieve details of a specific author.
- **Headers:**
  - Accept: application/json, application/xml
- **Response (JSON):**
    ```json
    {
        "id": 1, // integer
        "name": "Jane Austen", // string
        "birthdate": "1775-12-16", // string (date, YYYY-MM-DD)
        "biography": "Jane Austen was an English novelist known primarily for her six major novels." // string
    }
    ```
- **Response (XML):**
    ```xml
    <author>
        <id>1</id> <!-- integer -->
        <name>Jane Austen</name> <!-- string -->
        <birthdate>1775-12-16</birthdate> <!-- string (date, YYYY-MM-DD) -->
        <biography>Jane Austen was an English novelist known primarily for her six major novels.</biography> <!-- string -->
    </author>
    ```

#### Add a New Author

- **URL:** `/api/book/author`
- **Method:** `POST`
- **Description:** Add a new author.
- **Headers:**
  - Content-Type: application/json, application/xml
- **Request Body (JSON):**
    ```json
    {
        "name": "Aldous Huxley", // string
        "birthdate": "1894-07-26", // string (date, YYYY-MM-DD)
        "biography": "Aldous Huxley was an English writer and philosopher, author of Brave New World." // string
    }
    ```
- **Request Body (XML):**
    ```xml
    <author>
        <name>Aldous Huxley</name> <!-- string -->
        <birthdate>1894-07-26</birthdate> <!-- string (date, YYYY-MM-DD) -->
        <biography>Aldous Huxley was an English writer and philosopher, author of Brave New World.</biography> <!-- string -->
    </author>
    ```
- **Response (JSON):**
    ```json
    {
        "id": 5, // integer
        "name": "Aldous Huxley", // string
        "birthdate": "1894-07-26", // string (date, YYYY-MM-DD)
        "biography": "Aldous Huxley was an English writer and philosopher, author of Brave New World." // string
    }
    ```
- **Response (XML):**
    ```xml
    <author>
        <id>5</id> <!-- integer -->
        <name>Aldous Huxley</name> <!-- string -->
        <birthdate>1894-07-26</birthdate> <!-- string (date, YYYY-MM-DD) -->
        <biography>Aldous Huxley was an English writer and philosopher, author of Brave New World.</biography> <!-- string -->
    </author>
    ```

#### Update Author by ID

- **URL:** `/api/book/author/{id}`
- **Method:** `PUT`
- **Description:** Update an author's information.
- **Headers:**
  - Content-Type: application/json, application/xml
- **Request Body (JSON):**
    ```json
    {
        "name": "George Orwell", // string
        "birthdate": "1903-06-25", // string (date, YYYY-MM-DD)
        "biography": "George Orwell was an English novelist, essayist, journalist, and critic." // string
    }
    ```
- **Request Body (XML):**
    ```xml
    <author>
        <name>George Orwell</name> <!-- string -->
        <birthdate>1903-06-25</birthdate> <!-- string (date, YYYY-MM-DD) -->
        <biography>George Orwell was an English novelist, essayist, journalist, and critic.</biography> <!-- string -->
    </author>
    ```
- **Response (JSON):**
    ```json
    {
        "id": 6, // integer
        "name": "George Orwell", // string
        "birthdate": "1903-06-25", // string (date, YYYY-MM-DD)
        "biography": "George Orwell was an English novelist, essayist, journalist, and critic." // string
    }
    ```
- **Response (XML):**
    ```xml
    <author>
        <id>6</id> <!-- integer -->
        <name>George Orwell</name> <!-- string -->
        <birthdate>1903-06-25</birthdate> <!-- string (date, YYYY-MM-DD) -->
        <biography>George Orwell was an English novelist, essayist, journalist, and critic.</biography> <!-- string -->
    </author>
    ```

#### Delete Author by ID

- **URL:** `/api/book/author/{id}`
- **Method:** `DELETE`
- **Description:** Delete an author.
- **Headers:**
  - Accept: application/json, application/xml
- **Response (JSON):**
    ```json
    {
        "message": "Author deleted successfully" // string
    }
    ```
- **Response (XML):**
    ```xml
    <message>Author deleted successfully</message> <!-- string -->
    ```

### Actions

#### Borrow a Book

- **URL:** `/api/book/{id}/action/1`
- **Method:** `POST`
- **Description:** Borrow a book.
- **Headers:**
  - Content-Type: application/json, application/xml
- **Request Body (JSON):**
    ```json
    {
        "userId": 1, // integer
        "bookId": 1 // integer
    }
    ```
- **Request Body (XML):**
    ```xml
    <action>
        <userId>1</userId> <!-- integer -->
        <bookId>1</bookId> <!-- integer -->
    </action>
    ```
- **Response (JSON):**
    ```json
    {
        "message": "Book borrowed successfully", // string
    "borrowingId": 1 // integer
    }
    ```
- **Response (XML):**
    ```xml
    <response>
        <message>Book borrowed successfully</message> <!-- string -->
    <borrowing_d>1</borrowingId> <!-- integer -->
    </response>
    ```

#### Return a Book

- **URL:** `/api/book/{id}/action/2`
- **Method:** `POST`
- **Description:** Return a borrowed book.
- **Headers:**
  - Content-Type: application/json, application/xml
- **Request Body (JSON):**
    ```json
    {
    "borrowingId": 1, // integer
        "userId": 1, // integer
        "bookId": 1 // integer
    }
    ```
- **Request Body (XML):**
    ```xml
    <action>
    <borrowingId>1</borrowingId> <!-- integer -->
        <userId>1</userId> <!-- integer -->
        <bookId>1</bookId> <!-- integer -->
    </action>
    ```
- **Response (JSON):**
    ```json
    {
        "message": "Book returned successfully" // string
    }
    ```
- **Response (XML):**
    ```xml
    <response>
        <message>Book returned successfully</message> <!-- string -->
    </response>
    ```