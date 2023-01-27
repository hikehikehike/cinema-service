# Cinema service
API service for cinema management. Written in Python using Django REST Framework.

## Installing

Install PostgreSQL and create db

```shell
git clone https://github.com/hikehikehike/cinema-service
git checkout develop
python -m venv venv
venv\Scripts\activate (on Windows)
source venv/bin/activate (on macOS)
pip install -r requirements.txt
set DB_HOST=<your db hostname>
set DB_NAME=<your db name>
set DB_USER=<your db username>
set DB_PASSWORD=<your db user password>
set SECRET_KEY=<your secret key>
python manage.py migrate
python manage.py runserver
```

### Run with docker

Docker should be installed

```shell
docker-compose build
docker-compose up
```

### Getting access

- create user via /api/user/register/
- get access token via /api/user/token/

## Features

- JWT authenticated
- Admin panel /admin/
- Documentation is located at /api/doc/swagger/ or api/doc/redoc/
- Managing orders and tickets
- Creating movies with genres, actors and image
- Creating cinema halls
- Adding movie sessions
- Filtering movies and movie sessions