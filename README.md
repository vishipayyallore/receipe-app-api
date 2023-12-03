# Recipe Web API

Recipe API Project. I am learning this from a Video Course

## Steps

> 1. Create requirements.txt
> 1. Create Dockerfile
> 1. Create .dockerignore
> 1. Create docker-compose.yml
> 1. Create requirements.dev.txt (For Dev Dependencies. Example: Flake)

## 01-Dec-2023

```bash
docker build . -t recipe-api

docker-compose build
```

## 02-Dec-2023

```bash
docker-compose run --rm app sh -c "django-admin startproject app ."

docker-compose up

docker-compose run --rm app sh -c "flake8"

docker-compose up

docker-compose down

docker-compose run --rm app sh -c "python manage.py test"
```

## 03-Dec-2023

```bash
docker-compose run --rm app sh -c "python manage.py startapp core"

docker-compose run --rm app sh -c "python manage.py test"

docker-compose run --rm app sh -c "python manage.py wait_for_db"

docker-compose run --rm app sh -c "python manage.py test && flake8"
```

## Few Commands

```bash
docker build . -t recipe-api

docker-compose build

docker-compose run --rm app sh -c "flake8"

docker-compose run --rm app sh -c "django-admin startproject app ."

docker-compose up

docker-compose down

docker-compose run --rm app sh -c "python manage.py test"

docker-compose run --rm app sh -c "python manage.py startapp core"

docker-compose run --rm app sh -c "python manage.py wait_for_db"

docker-compose run --rm app sh -c "python manage.py test && flake8"

docker-compose run --rm app sh -c "python manage.py makemigrations"

docker-compose run --rm app sh -c "python manage.py wait_for_db && python manage.py migrate"

docker-compose down

docker volume rm recipe-app-api_dev-db-data

docker-compose run --rm app sh -c "python manage.py wait_for_db && python manage.py migrate && python manage.py test && flake8"

docker-compose run --rm app sh -c "python manage.py wait_for_db && python manage.py createsuperuser"

docker-compose run --rm app sh -c "python manage.py test"

docker-compose run --rm app sh -c "python manage.py test && flake8"
```

## Creating User App

We are going to create a user app. This will be used for authentication and authorization.

```bash
docker-compose run --rm app sh -c "python manage.py startapp user"

docker-compose run --rm app sh -c "python manage.py makemigrations"

docker-compose run --rm app sh -c "python manage.py wait_for_db && python manage.py migrate"

docker-compose run --rm app sh -c "python manage.py test && flake8"

docker compose -f "docker-compose.yml" up -d --build

docker compose up -d --build

Token aaa8aaaa07aa3aaa0218aa2a19a7022a665a843a
```

## Creating Recipe App

```bash
docker-compose run --rm app sh -c "python manage.py startapp recipe"

```
