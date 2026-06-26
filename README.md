# Strantell Website

Optimized Django project structure for the Strantell marketing website.

## Project structure

```text
strantell_website_optimized/
├── manage.py
├── requirements.txt
├── .env.example
├── .gitignore
├── core/
│   ├── static/core/css/styles.css
│   ├── static/core/img/
│   ├── templates/base.html
│   ├── templates/includes/navbar.html
│   └── templates/core/
└── strantell_site/
    ├── settings.py
    ├── urls.py
    ├── asgi.py
    └── wsgi.py
```

## Local setup

```cmd
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
copy .env.example .env
python manage.py migrate
python manage.py runserver
```

Then open:

```text
http://127.0.0.1:8000/
```

## Notes

- `.venv`, `.env`, `db.sqlite3`, `staticfiles`, and `__pycache__` are intentionally excluded.
- `STATIC_URL` is set to `/static/`.
- The navbar lives in `core/templates/includes/navbar.html` and is included by `base.html`.
- Page templates extend `base.html`.
