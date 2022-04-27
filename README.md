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

> 'git clone https://github.com/030722-VA-SRE/Alex-Pazmino.git'

- create system environment variables on your local device containing
 your database credentials
   - the names of the environment variables are: DB_URL, DB_USER, and DB_PASS

- navigate to the gameshop directory

'cd gameshop/'

- Run the docker-compose.yml to package and containerize the application

'docker-compose up -d'

## Usage 
Using Postman or a web browser

- As an Admin:
    * I can view all users.
       > GET localhost:8080/users
    * I can add a new user.
       > POST localhost:8080/users
    * I can update a user.
       > PUT localhost:8080/users/{id}
    
- As a User:
   * I can view all games.
      > GET localhost:8080/games
    * I can view games by ID.
      > GET localhost:8080/games/{id}
    * I can delete a game by ID.
      > DELETE localhost:8080/games/{id}
    * I can add a game.
      > POST localhost:8080/games
    * I can update a game by ID.
      > PUT localhost:8080/games/{id}

   * I can view all platforms.
       > GET localhost:8080/platforms
    * I can view platforms by ID.
       > GET localhost:8080/platforms/{id}
    * I can add a platform.
      > POST localhost:8080/platforms
    * I can update a platform by ID.
      > PUT localhost:8080/platforms/{id}
    * I can delete a platform by ID.
       > DELETE localhost:8080/platforms/{id}
       - NOTE: this will delete all games associated with said platform!
