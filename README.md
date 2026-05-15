# Django Blog Project

A full-featured Django web application with user authentication, a blog, and custom forms.

---

## Project Structure

```
├── accounts/           # User registration, login, and profile management
├── blog/               # Blog posts: creation, listing, and detail views
├── django_project/     # Core Django settings, URLs, and WSGI/ASGI config
├── static/css/         # Global stylesheets and static assets
├── templates/          # HTML templates shared across apps
├── manage.py           # Django management CLI
└── .gitignore
```

---

## Features

- **User Accounts** — Register, log in, log out, and manage user profiles
- **Blog** — Create, read, update, and delete blog posts
- **Forms** — Custom Django forms with validation
- **Static Files** — CSS served via Django's static file system
- **Templating** — Shared base templates with per-app overrides

---

## Requirements

- Python 3.8+
- Django 4.x

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Getting Started

**1. Clone the repository**

```bash
git clone https://github.com/JeanomWilliams/blog.git
cd blog
```

**2. Apply migrations**

```bash
python manage.py migrate
```

**3. Create a superuser** *(optional, for admin access)*

```bash
python manage.py createsuperuser
```

**4. Run the development server**

```bash
python manage.py runserver
```

Visit `http://127.0.0.1:8000` in your browser.

---

## Static Files

Static files are located in `static/css/`. To collect them for production:

```bash
python manage.py collectstatic
```

---

## Configuration

Core settings live in `django_project/settings.py`. Key settings to review before deploying:

- `SECRET_KEY` — replace with an environment variable
- `DEBUG` — set to `False` in production
- `ALLOWED_HOSTS` — add your domain
- `DATABASES` — defaults to SQLite; swap for PostgreSQL in production

---

## Admin

The Django admin panel is available at `/admin/` when the server is running. Log in with the superuser credentials created above.
