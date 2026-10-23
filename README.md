# VibeReads 📚

**A PHP and MySQL-powered online bookstore with mood-based book discovery.**

VibeReads is a web-based bookstore project that brings together book browsing, personalized discovery, and a simple online shopping workflow. Readers can explore books, view details, find titles based on their mood, add books to a shopping cart, and place orders through the website.

## Features

### Book browsing and discovery
- Browse the book catalog and view individual book details.
- Search for books.
- Explore the dedicated e-books page.
- Discover books through the **Mood Matcher**, which organizes recommendations around selected moods and genres.

### Shopping experience
- Add books to a shopping cart and review cart contents.
- Update the shopping flow through cart and checkout pages.
- Provide delivery and contact details at checkout and place orders.
- View order-related information.
- Generate an order invoice as a PDF using the included DOMPDF library.

### User experience
- Register, log in, and log out.
- Access a user profile page.
- Visit About Us and Contact Us pages.
- Manage cookie preferences through a dedicated page.

## Technology stack

| Layer | Technology |
| --- | --- |
| Backend | PHP |
| Database | MySQL |
| Database access | MySQLi |
| Frontend | HTML, CSS, JavaScript |
| PDF generation | DOMPDF (included with the project) |
| Local development | PHP-enabled web server and MySQL (for example, XAMPP) |

## Project structure

```text
VibeReads/
├── index.php                 # Home page
├── index_header.php          # Shared header
├── index_footer.php          # Shared footer
├── shop.php                  # Book catalog
├── search_books.php          # Book search
├── book_details.php          # Individual book details
├── ebooks.php                # E-books page
├── mood_matcher.php          # Mood-based discovery
├── cart.php                  # Shopping cart
├── add_to_cart.php           # Add-to-cart handler
├── checkout.php              # Checkout
├── orders.php                # Orders
├── invoice.php               # PDF invoice
├── register.php              # Registration
├── login.php                 # Login
├── logout.php                # Logout
├── profile.php               # User profile
├── about-us.php              # About page
├── contact-us.php            # Contact page
├── cookie-management.php     # Cookie preferences
├── config.php                # Database connection configuration
├── classes/                  # PHP classes
├── database/
│   └── vibeReadsdb.sql       # Database schema and included SQL data
├── dompdf/                   # Bundled PDF generation dependency
├── added_books/              # Book images
└── Books Picture/            # Book images
```

*The structure above highlights key files and folders, not every asset in the project.*

## Getting started

### Prerequisites
- PHP and a compatible local web server (such as Apache in XAMPP)
- MySQL or MariaDB
- A browser
- A tool such as phpMyAdmin to import the supplied SQL file

### 1. Download the project

Clone the repository using its GitHub URL, or download it as a ZIP and extract it.

```bash
git clone <YOUR-REPOSITORY-URL>
```

### 2. Put the project in your server's web directory

For XAMPP on Windows, copy the project folder into `C:\xampp\htdocs\` and rename the folder to `VibeReads` if desired.

### 3. Set up the database

1. Start **Apache** and **MySQL** in XAMPP.
2. Open `http://localhost/phpmyadmin`.
3. Create a database named `vibeReadsdb`.
4. Import `database/vibeReadsdb.sql` from the project folder.

### 4. Configure the database connection

The existing `config.php` uses these local development settings:

```php
$conn = new mysqli('localhost', 'root', '', 'vibeReadsdb');
```

Update the host, username, password, and database name in `config.php` to match your environment. **Do not commit real database passwords or other secrets to a public repository.** Some PHP pages also establish their own database connections, so check those settings if your credentials differ.

### 5. Run the application

Open:

```text
http://localhost/VibeReads/index.php
```

The URL depends on the folder name you use under `htdocs`.

## How it works

1. A visitor browses or searches the book catalog.
2. They can explore recommendations using Mood Matcher.
3. A registered user logs in and adds books to their cart.
4. The user reviews their cart, enters checkout details, and places an order.
5. Order pages and PDF invoice generation support order follow-up.

## Development concepts

This project provides experience with:

- Building multi-page web applications with PHP.
- Integrating PHP with a MySQL relational database.
- Implementing user sessions and account-related pages.
- Handling forms, book searches, cart operations, and order records.
- Organizing reusable code in PHP classes.
- Generating downloadable PDF documents.

## Notes

- This is a source-based description of the submitted project; features have not been end-to-end tested in a running environment.
- The checkout flow exists in the code, but **integration with an external payment gateway has not been verified**.
- Before deploying publicly, review authentication, input validation, SQL queries, secret handling, and the bundled dependencies for security.
- The provided SQL export may contain sample data. Review it before publishing the repository.

## Author

**Nethmi Wijekoon**

- [GitHub](https://github.com/nethukw)
- [LinkedIn](https://www.linkedin.com/in/nethukzz)
- [Portfolio](https://nethmi-wijekoon-portfolio.netlify.app/)

---

*VibeReads — discover books that match your mood.*
