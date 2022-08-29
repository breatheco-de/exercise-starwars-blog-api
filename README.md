# ![alt text](https://assets.breatheco.de/apis/img/images.php?blob&random&cat=icon&tags=breathecode,32) StarWars Blog API

It is recomended to develop this project in conjuntion with the [StarWars Blog Reading List](https://github.com/breatheco-de/exercise-starwars-blog-reading-list), you will eventually integrate both projects and have a fully functional applications with backend and front-end.

Today we are going to build one API to manage a blog (about StarWars), users on this blog will be able to list planets, list characters and create or remove favorites.

To allow users to do all of this, we must follow these steps:

1. Start by modeling the database: Create a database and the tables needed to store that information, you may have already done this when you did the StarWars DataModeling project in [python/flask](https://github.com/breatheco-de/exercise-starwars-data-modeling) or [node/express](https://github.com/breatheco-de/starwars-data-model-typeorm-node)
2. Build your endpoints using Flask or Express (depending on your cohort main language).
3. Constantly test your endpoitns with postman.

## 🌱  How to start this project

Do not clone this repository.

The first step to start coding is cloning the [flask](https://github.com/4GeeksAcademy/flask-rest-hello) or the [express.js](https://github.com/breatheco-de/starwars-data-model-typeorm-node) boilerplate (depending on your cohort main backend language).

a) If using Gitpod (recommended) you can clone the **python** boilerplate by [clicking here](https://github.com/4GeeksAcademy/flask-rest-hello) or the **node.js** boilerplate by [clicking here](https://github.com/4GeeksAcademy/expressjs-rest-hello).

b) If working locally type the following command from your command line: 
```sh
For Python/Flask:
$ git clone https://github.com/4GeeksAcademy/flask-rest-hello

For Node/Express.js:
$ git clone https://github.com/4GeeksAcademy/expressjs-rest-hello
```
(you will need to have a database installed and python 3.7+ installed if you do it locally but all of that it's already installed on Gitpod)
 

The boiplerplate's README files has a video on how to start and complete your API. 

🐍 For python: There is an interactive tutorial on how to build a [Flask API](https://github.com/breatheco-de/python-flask-api-tutorial), its a similar process but instead of `tasks` here you will be dealing with `people` and `planets`.


💡 Important: Remember to create a new repository, update the remote (`git remote set-url origin <your new url>`), and upload the code to your new repository using `add`, `commit` and `push`.

## 📝 Instructions

Create an API that connects to a database and implements the following Endpoints (very similar to SWAPI.dev or SWAPI.tech):

- `[GET] /people` Get a list of all the people in the database
- `[GET] /people/<int:people_id>` Get a one single people information
- `[GET] /planets` Get a list of all the planets in the database
- `[GET] /planets/<int:planet_id>` Get one single planet information

Aditionally create the following endpoints to allow your StarWars blog to have users and favorites:

- `[GET] /users` Get a list of all the blog post users.
- `[GET] /users/favorites` Get all the favorites that belong to the current user.
- `[POST] /favorite/planet/<int:planet_id>` Add a new favorite planet to the current user with the planet id = `planet_id`.
- `[POST] /favorite/people/<int:people_id>` Add a new favorite people to the current user with the people id = `people_id`.
- `[DELETE] /favorite/planet/<int:planet_id>` Delete favorite planet with the id = `planet_id`.
- `[DELETE] /favorite/people/<int:people_id>` Delete favorite people with the id = `people_id`.
- Your current API does not have an authentication system (yet), that is why the only way to create users is directly on the database using the flask admin.

☝️ Note: here is a sample API in Postman: 
https://documenter.getpostman.com/view/2432393/TzRSgnTS#a4174b48-3fc8-46e3-bf82-19a08107666f

## 📖 Fundamentals

This exercise will make you practice the following fundamentals:

1. Building an RESTful API using one of the most popular libraries [Python Flask](https://flask.palletsprojects.com/en/1.1.x/) or [Express.js](https://expressjs.com/).
2. Building a database with the **ORM** called [SQLAlchemy](https://www.sqlalchemy.org/) or [TypeORM](https://typeorm.io/)
3. Database Migrations using migration system [Alembic](https://alembic.sqlalchemy.org/en/latest/) or the native migration system from TypeORM.

## 😎 Feeling confident?

The following requirements are not necesary to successfully complete this project, but you want try coding them if you feel like challenging yourself ☺️

`+1` Create also an enpoint to add (POST), update (PUT), and delete (DELETE) planets and people, that way all the database information can be manage using the API instead of having to rely on the flask admin to create the plantes and people.
