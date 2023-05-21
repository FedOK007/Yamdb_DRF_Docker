# Educational project yamdb_final
![workflow action status](https://github.com/FedOK007/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)

## Discription

This project is a adapted to Docker and Docker-cpmpose api_yamdb project

### API Documentation:
Example and documentation - [http://51.250.102.154/redoc/](http://51.250.102.154/redoc/)

### Project api_yamdb description

Created on the basis of the framework [Django REST Framework (DRF)](https://github.com/ilyachch/django-rest-framework-rusdoc)

> The YaMDb project collects user reviews of works. The works are divided into categories: "Books", "Films", "Music".
> The works themselves are not stored in YaMDb, you can't watch a movie or listen to music here.
> In each category there are works: books, movies or music.
> A work can be assigned a genre from the preset list (for example, "Fairy Tale", "Rock" or "Arthouse").
> Grateful or outraged users leave text reviews for the works and rate the work, an average rating of the work is formed from user ratings.

## Technologies

- Python 3.7
- Django 3.2.15
- Docker version 20.10.24
- Docker-compose 3.8

## Start Project 
Clone the repository and go to it on the command line:

```
git clone git@github.com:FedOK007/yamdb_final.git
```

### **Run images with docker-copmpose**

Go to the directory infra

```
cd infra
```

Make .env file use .env_example and fill correct parameters

```
mv .env_example .env
nano .env
```

Run docker-compose up

```
docker-compose up
```

Next make migrations and run collectstatic inside the Image "web"

```
docker-compose exec web python manage.py migrate
```

Your app is available at: http://localhost

## Documentation Api (local)
Documentaion is available at http://127.0.0.1:8000/redoc or http://localhos/redoc for docker-compose installation.

### Request examples

> Get (http://127.0.0.1:8000/api/v1/categories/1):

```
{
  "name": "Film",
  "slug": "Movie"
}
```
## Authors

[FedOK007](https://github.com/FedOK007)