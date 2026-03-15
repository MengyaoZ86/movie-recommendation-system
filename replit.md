# CinemaRank - Movie Recommendation System

## Overview
Django-based movie recommendation system with collaborative filtering (user-based and item-based). Features movie browsing, search, filtering by tags, user ratings, collections, comments, and personalized recommendations.

## Tech Stack
- **Framework:** Django 4.2 (upgraded from 2.2 for Python 3.12 compatibility)
- **Database:** SQLite3 (`db.sqlite3`)
- **Frontend:** Bootstrap, jQuery, HTML templates
- **REST API:** Django REST Framework 3.15.2

## Project Structure
- `movierecomend/` - Django project settings, URLs, WSGI config
- `movie/` - Main app (models, views, forms, admin, migrations)
- `movie_it/` - Data population scripts, recommendation algorithms
- `templates/` - HTML templates
- `static/` - CSS, JS, images
- `media/` - Movie cover images
- `csv_data/` - CSV data files for seeding movies
- `populate_data/` - Data population utilities

## Running the App
- **Development:** `python manage.py runserver 0.0.0.0:5000`
- **Production:** `gunicorn --bind=0.0.0.0:5000 --reuse-port movierecomend.wsgi:application`
- **Port:** 5000

## Key Configuration
- `movierecomend/settings.py` - Django settings
  - `ALLOWED_HOSTS = ['*']` - All hosts allowed (required for Replit proxy)
  - `CSRF_TRUSTED_ORIGINS` - Replit domains trusted for CSRF
  - Database: SQLite3 at `db.sqlite3`
  - Media files served from `/media/`
  - Static files served from `/static/`

## Setup Notes
- Django was upgraded from 2.2 to 4.2 for Python 3.12 compatibility (`distutils` removal)
- DRF was upgraded from 3.13 to 3.15.2 for Django 4.2 compatibility
- Migrations are applied; database is ready
- Run `python manage.py createsuperuser` to create an admin account
- Admin panel at `/admin/`
