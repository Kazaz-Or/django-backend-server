# What's in the repo?

<h4>Backend REST API server built with Django framework</h4>
<h5>The application's scope is a recipes app - The users can post recipes (text and/or pictures) and filter them by specific tags or ingredients</h5>
<h5>This project was made as an educational project for learning proposes and inclueds only the backend</h5>


![CA554629-2D2C-443B-9D03-6C06C25D9100](https://user-images.githubusercontent.com/83350680/178946837-83d6271e-b409-47c5-9ba6-0b4d10a14e02.jpeg)


# Functionality:

<h4>19 API Endpoints:</h4>
<p>- Creating users (registration)</p>
<p>- Managing Login & User Authentication (Using Token authentication)</p>
<p>- Managing Recipes (POST, GET, PATCH, PUT, DELETE)</p>
<p>- Managing recipe tags (POST, GET, PATCH, PUT, DELETE)</p>
<p>- Managing recipe ingredients (POST, GET, PATCH, PUT, DELETE)</p>
<p>- Uploading (POST) recipe images via API endpoint</p>
<p>- Filtering (GET) according to the list of endpoints (user, tags, ingredients)</p>
<p>- Docs (Swagger OpenAPI UI)</p>
<p>- Admin Interface (Django Admin)</p>

<details>
  <summary>List of endpoints URLs</summary>
  <ol>
    <li>
      <h5>User:</h5></li>
      <ul>
        <li>POST create user (/api/user/create/)</li>
        <li>GET user (/api/user/me/)</li>
        <li>PUT user (/api/user/me)</li>
        <li>PATCH user (/api/user/me)</li>
        <li>POST login to get a token (/api/user/token/)</li>
      </ul>
      <li>
      <h5>Recipe:</h5></li>
      <ul>
        <li>GET recipes (/api/recipe/recipes/)</li>
        <li>POST recipes (/api/recipe/recipes/)</li>
        <li>GET recipe by id (/api/recipe/recipes/{id})</li>
        <li>PUT recipe by id (/api/recipe/recipes/{id})</li>
        <li>PATCH recipe by id (/api/recipe/recipes/{id})</li>
        <li>DELETE recipe by id (/api/recipe/recipes/{id})</li>
      </ul>
      <li>
      <h5>Ingredients:</h5></li>
      <ul>
        <li>GET recipe ingredients (/api/recipe/ingredients)</li>
        <li>PUT recipe ingredients (/api/recipe/ingredients/{id})</li>
        <li>PATCH recipe ingredients (/api/recipe/ingredients/{id})</li>
        <li>DELETE recipe ingredients (/api/recipe/ingredients/{id})</li>
      </ul>
      <li>
      <h5>Tags:</h5></li>
      <ul>
        <li>GET recipe tags (/api/recipe/tags)</li>
        <li>PUT recipe tags (/api/recipe/tags/{id})</li>
        <li>PATCH recipe tags (/api/recipe/tags/{id})</li>
        <li>DELETE recipe tags (/api/recipe/tags/{id})</li>
      </ul>
      <li>
      <h5>Recipe Image Upload:</h5></li>
      <ul>
        <li>POST recipe image (/api/recipe/recipes/{id}/upload-image/)</li>
      </ul>
  </ol>
</details>


# Application Strucuture:

- app/ - Django Project
- app/core/ - Shared code between multiple apps within the project
- app/user - User related code
- app/recipe/ - Recipe related code


# Docs:

<p>Documentation & Browsable API mainly for testing</p>

![F8436961-A1EA-47A7-8DAF-B795F61AC9D4_1_105_c](https://user-images.githubusercontent.com/83350680/178949734-af1ad1f2-1cac-4691-b0b7-94529808c7d8.jpeg)

```
http://172.0.0.1:8000/api/docs
```

https://user-images.githubusercontent.com/83350680/178953823-5f97031c-6958-40e6-8c87-0c26629da8d5.mov


# This projects covers the following:

- Python
- Django Framework (URL mappings, add-ons & django rest framework)
- Docker & Docker configuration
- Database (PostgreSQL)
- Docs (using drf-spectacular, including extend schemas)
- GitHub Actions (includes testing & linting)
- Test coverage using unittest & django testing framework
- Linter (using flake8)

# How to:

To run the application using docker-compose:
```
docker-compose build
docker-compose up
```
To stop the application:
```
docker-compose down
```
To run the tests:
```
docker-compose run --rm app sh -c "python manage.py test"
```
To run flake8 linter:
```
docker-compose run --rm app sh -c "python manage.py wait_for_db && flake8"
```
