# Bookshelf V2

ENGO 651 - Adv. Topics on Geospatial Technologies

By Adam and Chavisa

## Description

In this project, we utilize the [Google Books API](https://developers.google.com/books) to extend the functionality of our web app *Bookshelf*.  As in the [previous version](https://github.com/adamreidsmith/ENGO651-project1), users can create an account or log in to an existing account, and search for books by title, author, or ISBN.  Clicking on a search result displays more information about the book, including an average rating and rating count obtained from the Google Books API.  Users can also leave reviews and ratings for each book and see the reviews and ratings that other users have left.  Each user can add at most one review and rating to each book.

Our app also includes an API accessible via the `/api/<isbn>` route, where `<isbn>` is should be replaced with the 10-digit ISBN of the desired book.  No account is required to access the API, so anyone can use it.  The API returns the following information in JSON format:

        {
        "title": "Title",
        "author": "Author",
        "publishedDate": "Date",
        "ISBN_10": "ISBN_10",
        "ISBN_13": "ISBN_13", 
        "reviewCount": "Count", 
        "averageRating": "Rating" 
        }

If a field is not available, `Null` will be returned for that field.  If the requested ISBN is invalid or the book is not available in our database, a 404 error will be raised.

## File descriptions

The file [import.py](./import.py) creates 3 tables in the database and populates the *books* table with the book information provided in [books.csv](./books.csv).  The backend logic of the application is implemented in [application.py](./application.py).  This file instantiates the Flask application, handles the sign-in/sign-up logic as well as all database queries, and handles requests to the Google Books API.  The [templates](./templates) directory contains the HTML files for each page.  The home page, sign-in/sign-up pages, error pages, and success page all inherit from the [layout.html](./templates/layout.html) template.  The [search.html](./templates/search.html) page allows the user to search for books and displays the matching book titles as clickable results.  When a result is clicked, the [book.html](./templates/book.html) page displays further information about the book, some of which is obtained from the Google Books API.  The book page also allows the user to submit a review and rating for each book, as well as view reviews and ratings from other users.  All styling is contained in the file [style.css](./static/style.css) located in the [static](./static) directory.  Finally, [requirements.txt](requirements.txt) lists the dependencies of the project, and [books.csv](books.csv) contains the books available on our webapp.