# Cinema API

This is a Django REST framework (DRF) API for a cinema app. It provides endpoints for managing movies, cinema halls, orders and tickets, as well as user authentication and authorization. The API is designed to be consumed by front-end clients, mobile apps, or other third-party services, and can be extended and customized to fit specific requirements

## Installation

##### Clone the repository

```bash
git clone https://github.com/SergiiMachulin/Cinema-API.git
```

##### Change to the project directory

```bash
cd cinema-api
```

##### Create a virtual environment

```bash
python3 -m venv venv
```

##### Activate the virtual environment

```bash
source venv/bin/activate
```

##### Install the dependencies

```bash
pip install -r requirements.txt
```

##### Install PostgreSQL and create database.

Set the required environment variables in ```.env```file (need to be created, see example - ```.env.sample``` file):

`POSTGRES_DB`

`POSTGRES_USER`

`POSTGRES_PASSWORD`

`POSTGRES_HOST`


## Run Locally

### Environment Variables

Before run this project, add the following environment variables to your ```.env``` file

`DJANGO_SECRET_KEY`

`ALLOWED_HOSTS`

##### Run the database migrations

```bash
python manage.py migrate
```

 ##### Start the development server

```bash
python manage.py runserver
```

## Run with docker

1. Install Docker
2. Then:
```bash
docker-compose up --build
```

## Getting access
1. Create a new user at the following URL http://localhost:8000/api/user/register/

2. Obtain an access token at the following URL http://localhost:8000/api/user/token/


## Features

- JWT authenticated
- Admin panel /admin/
- Managing orders and tickets
- Creating movies with genres and actors
- Creating Cinema halls
- Adding movies sessions
- Filtering movies and movie sessions

## API Documentation

The API documentation is generated with drf-spectacular and can be accessed at the following URLs:

- Swagger UI: http://localhost:8000/api/doc/swagger/
- ReDoc: http://localhost:8000/api/doc/redoc/
