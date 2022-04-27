# Game Shop API

Online Item Shop Application

## Project Description

This shop is designed to display available games and the platforms that they are assigned to. Users are allowed to create, read, update, and delete games and platforms while admin is allowed to do the same with users.

## Technologies Used

- Java
- Maven
- Git
- Log4J
- JDBC
- Spring Boot 
- Spring MVC
- Spring Data JPA
- PostgreSQL
- JUnit
- Mockito
- Docker
- Promtail
- Loki
- Grafana
- Prometheus

## Features

Users can: 
   - see all available platforms
   - see all available games within the platforms
   - add new games/platforms
   - update games/platforms
   - delete games/platforms

Admin users can: 

   - see all users
   - add new users
   - update users
   - delete users

To-do list:

- Add more user-authorized actions
- generate owners of games and platforms
- enable purchasing of items
- More metric monitoring 

## Getting Started
- Clone Repository using Git Bash

'git clone https://github.com/030722-VA-SRE/Alex-Pazmino.git'

-create system environment variables on your local device containing
 your database credentials
- the names of the environment variables are: DB_URL, DB_USER, and DB_PASS

- navigate to the gameshop directory

'cd gameshop/'

- Run the docker-compose.yml to package and containerize the application

'docker-compose up -d'

## Usage 
- As an Admin:
    * I can view all users.
       > GET localhost:8080/users
    * I can add a new user.
       > POST localhost:8080/users
    * I can update a user.
       > PUT localhost:8080/users/{id}
        
    As a user, I can view all games.
        GET localhost:8080/games
    As a user, I can view games by ID.
        GET localhost:8080/games/{id}
    As a user, I can delete a game.
        DELETE localhost:8080/games/{id}
