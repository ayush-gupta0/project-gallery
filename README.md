# My Gallery

A minimal Django-based photo gallery with user accounts and media management.

This starter README is paired with a small skeleton for a `gallery` app (models and urls) plus an `.env.example` you can copy into your project.

---

## Features

- User accounts (Django auth) — sign up, login, logout
- Albums & photos (basic models: `Album`, `Photo`)
- Admin-ready (registers models)
- Local media storage in development; ready for SQLite/PostgreSQL

## Tech Stack

- **Backend:** Django (Python)
- **Database:** SQLite by default, PostgreSQL recommended for production
- **Auth:** Django session-based auth
- **Static/Media:** Django `staticfiles`; local media in dev

---

## Getting Started

### 1) Clone

```bash
git clone https://github.com/ayush-gupta0/project-gallery.git
cd project-gallery
```

### 2) Python & Virtualenv

```bash
python -m venv .venv
# Windows
. .venv/Scripts/activate
# macOS/Linux
source .venv/bin/activate
```

### 3) Install dependencies

```bash
pip install --upgrade pip
pip install -r requirement.txt
```

> The repo includes `requirement.txt` at the root.

### 4) Environment variables

Copy `.env.example` to `.env` and edit values:

```bash
cp .env.example .env
```

`.env.example` contains:

```env
DJANGO_SECRET_KEY=change-me
DJANGO_DEBUG=True
DATABASE_URL=sqlite:///db.sqlite3
ALLOWED_HOSTS=127.0.0.1,localhost
MEDIA_ROOT=.\media
STATIC_ROOT=.\staticfiles
```

If you are **not** using `DATABASE_URL`, configure `DATABASES` directly in `settings.py` (Django defaults to SQLite).

### 5) Database & superuser

```bash
python manage.py migrate
python manage.py createsuperuser
```

### 6) Run dev server

```bash
python manage.py runserver
```

Visit: http://127.0.0.1:8000/

---

## Project Structure (high level)

```
project-gallery/
├─ account/        # user auth & profiles (if present)
├─ galleria/       # gallery-related logic (if present)
├─ gallery/        # sample album/photo app (skeleton included in this pack)
├─ manage.py
├─ requirement.txt
└─ README.md
```
