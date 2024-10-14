![Django Logo](polls/static/img/Django-LOGO.png)

# Writing your first Django app

> This is a replica of the **Django Tutorial**. You can check on the [Django Documentation](https://docs.djangoproject.com/en/5.1/intro/)

## How to get Django
Django is available open-source under the BSD license. We recommend using the latest version of Python 3. The last version to support Python 2.7 is Django 1.11 LTS. See the FAQ for the Python versions supported by each version of Django. Here’s how to get it:

### Option 1: Get the latest official version
#### Linux / macOS:
```
python -m pip install Django==5.1.2
```
#### Windows:
```
py -m pip install Django==5.1.2
```

### Option 2: Get the latest development version
The latest and greatest Django version is the one that’s in our Git repository (our revision-control system). This is only for experienced users who want to try incoming changes and help identify bugs before an official release. Get it using this shell command, which requires [Git](https://git-scm.com/):
```
git clone https://github.com/django/django.git
```

## Set up a database
This step is only necessary if you’d like to work with a “large” database engine like PostgreSQL, MariaDB, MySQL, or Oracle. To install such a database, consult the [database installation information](https://docs.djangoproject.com/en/5.1/topics/install/#database-installation).

### Details on Database
If you plan to use Django’s database API functionality, you’ll need to make sure a database server is running. Django supports many different database servers and is officially supported with PostgreSQL, MariaDB, MySQL, Oracle and SQLite.

If you are developing a small project or something you don’t plan to deploy in a production environment, SQLite is generally the best option as it doesn’t require running a separate server. However, SQLite has many differences from other databases, so if you are working on something substantial, it’s recommended to develop with the same database that you plan on using in production.

To use another database other than SQLite, you’ll need to make sure that the appropriate Python database bindings are installed:
- If you’re using PostgreSQL, you’ll need the [psycopg](https://www.psycopg.org/psycopg3/) or [psycopg2](https://www.psycopg.org/) package. Refer to the [PostgreSQL notes](https://docs.djangoproject.com/en/5.1/ref/databases/#postgresql-notes) for further details.
- If you’re using MySQL or MariaDB, you’ll need a [DB API driver](https://docs.djangoproject.com/en/5.1/ref/databases/#mysql-db-api-drivers) like **mysqlclient**. See [notes for the MySQL backend](https://docs.djangoproject.com/en/5.1/ref/databases/#mysql-notes) for details.
- If you’re using SQLite you might want to read the [SQLite backend notes](https://docs.djangoproject.com/en/5.1/ref/databases/#sqlite-notes).
- If you’re using Oracle, you’ll need to install [oracledb](https://oracle.github.io/python-oracledb/), but please read the [notes for the Oracle backend](https://docs.djangoproject.com/en/5.1/ref/databases/#oracle-notes) for details regarding supported versions of both Oracle and **oracledb**.
- If you’re using an unofficial 3rd party backend, please consult the documentation provided for any additional requirements.

And ensure that the following keys in the 'default' item of the DATABASES dictionary match your database connection settings:
- **ENGINE** – Either **'django.db.backends.sqlite3'**, **'django.db.backends.postgresql'**, **'django.db.backends.mysql'**, or **'django.db.backends.oracle'**. Other backends are [also available](https://docs.djangoproject.com/en/5.1/ref/databases/#third-party-notes).
- **NAME** – The name of your database. If you’re using SQLite, the database will be a file on your computer. In that case, **NAME** should be the full absolute path, including the filename of that file. You don’t need to create anything beforehand; the database file will be created automatically when needed. The default value, **BASE_DIR / 'db.sqlite3'**, will store the file in your project directory.

If you are not using SQLite as your database, additional settings such as **USER**, **PASSWORD**, and **HOST** must be added. For more details, see the reference documentation for [DATABASES](https://docs.djangoproject.com/en/5.1/ref/settings/#std-setting-DATABASES).


# [Part 1](https://docs.djangoproject.com/en/5.1/intro/tutorial01/)

Let’s learn by example.

Throughout this tutorial, we’ll walk you through the creation of a basic poll application.

It’ll consist of two parts:

A public site that lets people view polls and vote in them.
An admin site that lets you add, change, and delete polls.


## Directory Hierarchy
```
|—— db.sqlite3
|—— manage.py
|—— mysite
|    |—— asgi.py
|    |—— settings.py
|    |—— urls.py
|    |—— wsgi.py
|    |—— __init__.py
|    |—— __pycache__
|        |—— settings.cpython-312.pyc
|        |—— urls.cpython-312.pyc
|        |—— wsgi.cpython-312.pyc
|        |—— __init__.cpython-312.pyc
|—— polls
|    |—— admin.py
|    |—— apps.py
|    |—— migrations
|        |—— 0001_initial.py
|        |—— __init__.py
|        |—— __pycache__
|            |—— 0001_initial.cpython-312.pyc
|            |—— __init__.cpython-312.pyc
|    |—— models.py
|    |—— static
|        |—— img
|            |—— Django-LOGO.png
|    |—— templates
|        |—— polls
|            |—— detail.html
|            |—— index.html
|            |—— results.html
|    |—— tests.py
|    |—— urls.py
|    |—— views.py
|    |—— __init__.py
|    |—— __pycache__
|        |—— admin.cpython-312.pyc
|        |—— apps.cpython-312.pyc
|        |—— models.cpython-312.pyc
|        |—— tests.cpython-312.pyc
|        |—— urls.cpython-312.pyc
|        |—— views.cpython-312.pyc
|        |—— __init__.cpython-312.pyc
```

## Code Details
### Tested Platform
- software
  ```
  OS: Debian unstable (May 2021), Ubuntu LTS
  Python: 3.8.5 (anaconda)
  PyTorch: 1.7.1, 1.8.1
  ```
- hardware
  ```
  CPU: Intel Xeon 6226R
  GPU: Nvidia RTX3090 (24GB)
  ```

### Hyper parameters
```
```
## References
- [paper-1]()
- [paper-2]()
- [code-1](https://github.com)
- [code-2](https://github.com)
  
## License

## Citing
If you use xxx,please use the following BibTeX entry.
```
```
