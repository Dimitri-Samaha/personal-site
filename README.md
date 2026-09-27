# Personal Site

The Django backend of an old personal portfolio site (originally hosted as `DimitriSamaha.github.io`; the Jekyll/GitHub Pages configuration has been removed — this is just the Django app that used to live alongside it).

## Apps
- **`main`** — a single landing-page app (`main/templates/main/index.html`).

## Tech stack
Python, Django, MySQL.

## Requirements
```
pip install django mysqlclient
```
`django_website02/settings.py` is configured to use MySQL directly (`ENGINE: django.db.backends.mysql`, database `django_website02`, host `127.0.0.1:3306`, user `root` / password `root`). A local MySQL server with those credentials and a `django_website02` database is required before `migrate` will succeed.

## Running it
```
mysql -u root -p -e "CREATE DATABASE django_website02"
python manage.py migrate
python manage.py runserver
```
Then open http://127.0.0.1:8000/.
