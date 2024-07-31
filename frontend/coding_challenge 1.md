Coding Challenge: CRUD Application for a Book Collection

# Objective:

Develop a simple web application that allows users to perform CRUD (Create, Read, Update, Delete) operations on a book collection. This application `MUST` be built using CodeIgniter 3.1.13 for the backend and Vue 2 for the frontend. The application should demonstrate your ability to handle both server-side and client-side development using an on-page Vue app i.e. not single page application, and basic styling using css.

# Technologies:

-   Backend: CodeIgniter 3.1.13 (PHP)
-   Frontend: Vue 2 (JavaScript)
-   Database: MySQL

# Task Requirements:

## Database Setup

Create a database table named books with the following columns:

```
id (INT, auto-increment, primary key)
title (VARCHAR, not null)
author (VARCHAR, not null)
genre (VARCHAR, not null)
published_year (YEAR, not null)
description (TEXT)
```

## Backend Development (CodeIgniter 3)

Controller: `Books`

Index Method: List all books
Create Method: Insert a new book. (via ajax request)
Retrieve Method: Retrieve a specific book by id.
Update Method: Update an existing book by id. (via ajax request)
Delete Method: Delete a book by id.

Model: `Book_model`

Methods to handle database interactions:

```
get_books(): Retrieve all books.
get_book($id): Retrieve a book by id.
create_book(): Insert a new book.
update_book(): Update a book by id.
delete_book($id): Delete a book by id.
```

Use query builder functions e.g. from, get_where, update etc

Routes:

```
GET /books → Books::get_books
POST /books/create → Books::create_book
GET /books/{id} → Books::get_book
POST /books/{id} → Books::update_book
GET /books/delete/{id} → Books::delete_book
```

## Frontend Development (Vue 2)

Create 3 pages:

1.  Page listing all books. `CAN` be vue app

1.          Page for creating new book. `CAN` be vue app

    Provide a form for adding new books.

1.  Page for viewing/editing single book. `MUST` be vue app

    Include a container `<div id="app"></div>` where the Vue instance will mount.

    Initialize a Vue instance that will manage the entire application within a single `<div id="app"></div>`

    Use the following Vue features:

    -   Data properties to hold the list of books and form inputs.
    -   2 way data binding using v-model
    -   Text interpolation using the “Mustache” syntax
    -   v-bind directive for CSS class names
    -   Methods to handle CRUD operations by making API calls using `fetch`.
    -   Event handling for form submissions and button clicks.

## API Integration

Use AJAX requests to the backend.

```
POST /books/create to create a new book
POST /books/{id} to update a book
```

## Validation and Error Handling

Where appropriate include frontend and/or backend to validate data.

-   Auther MUST be a firstname and lastname
-   Description must be at least 100 characters.

## User Interface

-   Create a clean and user-friendly interface using basic CSS. You can use a framework like Bootstrap for styling if desired.
-   Ensure the application is responsive and works well on different screen sizes.

## Submission Guidelines:

Push your code to a public repository on GitHub or another code hosting platform. Provide a link to the repository

README File: Ensure your README file includes:

-   Challenges you faced and how you addressed them.

## Evaluation Criteria:

-   Functionality: Does the application perform all CRUD operations as specified?
-   Code Quality: Is the code well-structured, readable, and maintainable?
-   Frontend: Is the user interface clean, intuitive, and responsive?
-   Backend: Are the database interactions and server-side logic efficiently implemented?
-   Validation: Are both client-side and server-side validations implemented effectively?
