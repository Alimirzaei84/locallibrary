# Local Library

**Local Library** is a Django 5.1.1 web application for managing a local library's catalog and lending system.

## Features

- **Catalog Browsing**: List and detail pages for books, authors, genres, and languages built with Django's generic class-based views and pagination.
- **Book Instances Management**: Tracks individual copies via a UUID field, status choices (maintenance, on loan, available, reserved), and borrower relationships.
- **User Authentication & Permissions**: Integrates Django's authentication system for login/logout and permission-based views; employs permission mixins for librarian functions.
- **Librarian Tools**: Provides views for librarians to view all borrowed books and renew due dates via a custom form (`RenewBookForm`) with validation citeturn10view0turn9view0.
- **Admin Interface**: Preconfigured Django admin with custom `ModelAdmin` classes for inline editing of related models citeturn11view0.
- **Responsive UI**: Uses Bootstrap 5 for layout, a custom sidebar navigation template, and static CSS enhancements.

## Installation

1. Clone the repo:
   ```bash
   git clone https://github.com/Alimirzaei84/locallibrary.git
   ```  
2. Create and activate a virtual environment:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```  
3. Install dependencies:
   ```bash
   pip install django==5.1.1
   ```  
4. Apply migrations and create a superuser:
   ```bash
   python manage.py migrate
   python manage.py createsuperuser
   ```  
5. Run the server:
   ```bash
   python manage.py runserver
   ```  

## Usage

- Navigate to `http://127.0.0.1:8000/catalog/` to browse the catalog.
- Use `http://127.0.0.1:8000/accounts/login/` to log in for borrowing and librarian options.
- Access the admin interface at `http://127.0.0.1:8000/admin/`.

## Project Structure

```
locallibrary/
├── catalog/           # Main application (models, views, templates, static) 
├── locallibrary/      # Project configuration (settings, URLs, WSGI/ASGI)
├── templates/         # Global templates (e.g., registration) 
├── db.sqlite3         # SQLite database
└── manage.py          # Django CLI utility
```

## License

MIT License.

