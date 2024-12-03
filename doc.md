# API Documentation

## Endpoints

### Books

#### Get All Books

- **URL:** `/api/book`
- **Method:** `GET`
- **Description:** Retrieve a list of all books.
- **Response (JSON):**
    ```json
    [
        {
            "id": 1,
            "title": "Pride and Prejudice",
            "author": "Jane Austen",
            "published_date": "1813-01-28",
            "genre": "Romance"
        },
        {
            "id": 2,
            "title": "I hope this doesn't find you",
            "author": "Ann Liang",
            "published_date": "2022-05-10",
            "genre": "Young Adult"
        },
        {
            "id": 3,
            "title": "1984",
            "author": "George Orwell",
            "published_date": "1949-06-08",
            "genre": "Dystopian"
        },
        {
            "id": 4,
            "title": "To Kill a Mockingbird",
            "author": "Harper Lee",
            "published_date": "1960-07-11",
            "genre": "Fiction"
        }
    ]
    ```
- **Response (XML):**
    ```xml
    <books>
        <book>
            <id>1</id>
            <title>Pride and Prejudice</title>
            <author>Jane Austen</author>
            <published_date>1813-01-28</published_date>
            <genre>Romance</genre>
        </book>
        <book>
            <id>2</id>
            <title>I hope this doesn't find you</title>
            <author>Ann Liang</author>
            <published_date>2022-05-10</published_date>
            <genre>Young Adult</genre>
        </book>
        <book>
            <id>3</id>
            <title>1984</title>
            <author>George Orwell</author>
            <published_date>1949-06-08</published_date>
            <genre>Dystopian</genre>
        </book>
        <book>
            <id>4</id>
            <title>To Kill a Mockingbird</title>
            <author>Harper Lee</author>
            <published_date>1960-07-11</published_date>
            <genre>Fiction</genre>
        </book>
    </books>
    ```

#### Get Book by ID

- **URL:** `/api/book/{id}`
- **Method:** `GET`
- **Description:** Retrieve details of a specific book.
- **Response (JSON):**
    ```json
    {
        "id": 1,
        "title": "1984",
        "author": "George Orwell",
        "published_date": "1949-06-08",
        "summary": "A dystopian social science fiction novel and cautionary tale about the dangers of totalitarianism.",
        "genre": "Dystopian"
    }
    ```
- **Response (XML):**
    ```xml
    <book>
        <id>1</id>
        <title>1984</title>
        <author>George Orwell</author>
        <published_date>1949-06-08</published_date>
        <summary>A dystopian social science fiction novel and cautionary tale about the dangers of totalitarianism.</summary>
        <genre>Dystopian</genre>
    </book>
    ```

#### Add a New Book

- **URL:** `/api/book`
- **Method:** `POST`
- **Description:** Add a new book.
- **Request Body (JSON):**
    ```json
    {
        "title": "Brave New World",
        "author": "Aldous Huxley",
        "published_date": "1932-08-30",
        "summary": "A dystopian social science fiction novel set in a futuristic World State.",
        "genre": "Dystopian"
    }
    ```
- **Request Body (XML):**
    ```xml
    <book>
        <title>Brave New World</title>
        <author>Aldous Huxley</author>
        <published_date>1932-08-30</published_date>
        <summary>A dystopian social science fiction novel set in a futuristic World State.</summary>
        <genre>Dystopian</genre>
    </book>
    ```
- **Response (JSON):**
    ```json
    {
        "id": 5,
        "title": "Brave New World",
        "author": "Aldous Huxley",
        "published_date": "1932-08-30",
        "summary": "A dystopian social science fiction novel set in a futuristic World State.",
        "genre": "Dystopian"
    }
    ```
- **Response (XML):**
    ```xml
    <book>
        <id>5</id>
        <title>Brave New World</title>
        <author>Aldous Huxley</author>
        <published_date>1932-08-30</published_date>
        <summary>A dystopian social science fiction novel set in a futuristic World State.</summary>
        <genre>Dystopian</genre>
    </book>
    ```

#### Update Book by ID

- **URL:** `/api/book/{id}`
- **Method:** `PUT`
- **Description:** Update details of an existing book.
- **Request Body (JSON):**
    ```json
    {
        "title": "Animal Farm",
        "author": "George Orwell",
        "published_date": "1945-08-17",
        "summary": "A satirical allegorical novella reflecting events leading up to the Russian Revolution of 1917.",
        "genre": "Political Satire"
    }
    ```
- **Request Body (XML):**
    ```xml
    <book>
        <title>Animal Farm</title>
        <author>George Orwell</author>
        <published_date>1945-08-17</published_date>
        <summary>A satirical allegorical novella reflecting events leading up to the Russian Revolution of 1917.</summary>
        <genre>Political Satire</genre>
    </book>
    ```
- **Response (JSON):**
    ```json
    {
        "id": 6,
        "title": "Animal Farm",
        "author": "George Orwell",
        "published_date": "1945-08-17",
        "summary": "A satirical allegorical novella reflecting events leading up to the Russian Revolution of 1917.",
        "genre": "Political Satire"
    }
    ```
- **Response (XML):**
    ```xml
    <book>
        <id>6</id>
        <title>Animal Farm</title>
        <author>George Orwell</author>
        <published_date>1945-08-17</published_date>
        <summary>A satirical allegorical novella reflecting events leading up to the Russian Revolution of 1917.</summary>
        <genre>Political Satire</genre>
    </book>
    ```

#### Delete Book by ID

- **URL:** `/api/book/{id}`
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

- **URL:** `/api/author`
- **Method:** `GET`
- **Description:** Retrieve a list of all authors.
- **Response (JSON):**
    ```json
    [
        {
            "id": 1,
            "name": "Jane Austen",
            "birthdate": "1775-12-16"
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
    <authors>
        <author>
            <id>1</id>
            <name>Jane Austen</name>
            <birthdate>1775-12-16</birthdate>
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
    </authors>
    ```

#### Get Author by ID

- **URL:** `/api/author/{id}`
- **Method:** `GET`
- **Description:** Retrieve details of a specific author.
- **Response (JSON):**
    ```json
    {
        "id": 1,
        "name": "Jane Austen",
        "birthdate": "1775-12-16",
        "biography": "Jane Austen was an English novelist known primarily for her six major novels."
    }
    ```
- **Response (XML):**
    ```xml
    <author>
        <id>1</id>
        <name>Jane Austen</name>
        <birthdate>1775-12-16</birthdate>
        <biography>Jane Austen was an English novelist known primarily for her six major novels.</biography>
    </author>
    ```

#### Add a New Author

- **URL:** `/api/author`
- **Method:** `POST`
- **Description:** Add a new author.
- **Request Body (JSON):**
    ```json
    {
        "name": "Aldous Huxley",
        "birthdate": "1894-07-26",
        "biography": "Aldous Huxley was an English writer and philosopher, author of Brave New World."
    }
    ```
- **Request Body (XML):**
    ```xml
    <author>
        <name>Aldous Huxley</name>
        <birthdate>1894-07-26</birthdate>
        <biography>Aldous Huxley was an English writer and philosopher, author of Brave New World.</biography>
    </author>
    ```
- **Response (JSON):**
    ```json
    {
        "id": 5,
        "name": "Aldous Huxley",
        "birthdate": "1894-07-26",
        "biography": "Aldous Huxley was an English writer and philosopher, author of Brave New World."
    }
    ```
- **Response (XML):**
    ```xml
    <author>
        <id>5</id>
        <name>Aldous Huxley</name>
        <birthdate>1894-07-26</birthdate>
        <biography>Aldous Huxley was an English writer and philosopher, author of Brave New World.</biography>
    </author>
    ```

#### Update Author by ID

- **URL:** `/api/author/{id}`
- **Method:** `PUT`
- **Description:** Update an author's information.
- **Request Body (JSON):**
    ```json
    {
        "name": "George Orwell",
        "birthdate": "1903-06-25",
        "biography": "George Orwell was an English novelist, essayist, journalist, and critic."
    }
    ```
- **Request Body (XML):**
    ```xml
    <author>
        <name>George Orwell</name>
        <birthdate>1903-06-25</birthdate>
        <biography>George Orwell was an English novelist, essayist, journalist, and critic.</biography>
    </author>
    ```
- **Response (JSON):**
    ```json
    {
        "id": 6,
        "name": "George Orwell",
        "birthdate": "1903-06-25",
        "biography": "George Orwell was an English novelist, essayist, journalist, and critic."
    }
    ```
- **Response (XML):**
    ```xml
    <author>
        <id>6</id>
        <name>George Orwell</name>
        <birthdate>1903-06-25</birthdate>
        <biography>George Orwell was an English novelist, essayist, journalist, and critic.</biography>
    </author>
    ```

#### Delete Author by ID

- **URL:** `/api/author/{id}`
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

- **URL:** `/api/book/{id}/action/1`
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

- **URL:** `/api/book/{id}/action/2`
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