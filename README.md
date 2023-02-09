# Bookshelf V2

ENGO 651 - Adv. Topics on Geospatial Technologies

By Adam and Chavisa

## Description

In this project, we utilize the [Google Books API](https://developers.google.com/books) to extend the functionality of our web app *Bookshelf*.  As in the [previous version](https://github.com/adamreidsmith/ENGO651-project1), users can create an account or log in to an existing account, and search for books by title, author, or ISBN.  Clicking on a search result displays more information about the book, including an average rating and rating count obtained from the Google Books API.  Users can also leave reviews and ratings for each book and see the reviews and ratings that other users have left.  Each user can add at most one review and rating to each book.

Our app also includes an API accessible via the `/api/<isbn>` route, where `<isbn>` is should be replaced with the 10 digit ISBN of the desired book.  No account is required to access the API, so anyone can use it.  



<!-- Here, we implement a book review website called *Bookshelf* using the web framework [Flask](https://flask.palletsprojects.com/en/2.2.x/) and the [PostgreSQL](https://www.postgresql.org) database system. This website allows registered users to search for books and leave reviews for books.  On the home page, users are prompted to either sign in or sign up for the website.  The webapp is inaccessible unless users sign up.  Once signed in, users can search for books by title, author, or ISBN, and view further information about each book by clicking the title.  On the book page, users can leave reviews for books and see reviews other users have left.

## File descriptions

The file [import.py](./import.py) creates 3 tables in the database and populates the *books* table with the book information provided in [books.csv](./books.csv).  The backend logic of the application is implemented in [application.py](./application.py).  This file instantiates the Flask application and handles the sign-in/sign-up logic as well as all database queries.  The [templates](./templates) directory contains the HTML files for each page.  The home page, sign-in/sign-up pages, error page, and success page all inherit from the [layout.html](./templates/layout.html) template.  The [search.html](./templates/search.html) page allows the user to search for books and displays the matching book titles as clickable results.  When a result is clicked, the [book.html](./templates/book.html) page displays further information about the book as well as a review section which allows users to view and post reviews of the book.  All styling is contained in the file [style.css](./static/style.css) located in the [static](./static) directory.  Finally, [requirements.txt](requirements.txt) lists the dependencies of the project. -->