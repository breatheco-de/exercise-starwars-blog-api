<!--hide-->
# StarWars Blog API
<!--endhide--> 

It is recommended to develop this project in conjunction with the [StarWars Blog Reading List](https://github.com/breatheco-de/exercise-starwars-blog-reading-list), you will eventually integrate both projects and have fully functional applications with back-end and front-end.

Today we are going to build an API to manage a blog (about StarWars). Users on this blog will be able to list planets, list characters, and create or remove favorites.

To allow users to do all of this, we must follow these steps:

1. Start by modeling the database: Create a database and the tables needed to store that information. You may have already done this when you did the StarWars Data Modeling project in [python/flask](https://github.com/breatheco-de/exercise-starwars-data-modeling) or [node/express](https://github.com/breatheco-de/starwars-data-model-typeorm-node).
2. Build your endpoints using Flask or Express (depending on your cohort's main language).
3. Constantly test your endpoints with [Postman](https://www.postman.com/).

<onlyfor saas="false" withBanner="false">
 
## 🌱 How to start this project

Do not clone this repository because we are going to be using a different template.

We recommend opening the `flask template` or the `express.js template` using a provisioning tool like [Codespaces](https://4geeks.com/lesson/what-is-github-codespaces) (recommended) or [Gitpod](https://4geeks.com/lesson/how-to-use-gitpod). Alternatively, you can clone it on your local computer using the `git clone` command.

These are the repositories you need to open or clone:

```txt
🐍 For Python/Flask:
https://github.com/4GeeksAcademy/flask-rest-hello

👩🏽‍💻 For Node/Express.js:
https://github.com/4GeeksAcademy/expressjs-rest-hello
```

> ⚠ You will need to have a database installed and Node.js or Python 3.7+ installed if you do it locally, but all of that is already installed on Codespaces or Gitpod.
 
The boilerplate's README files have a video on how to start and complete your API. 

🐍 For Python: There is an interactive tutorial on how to build a [Flask API](https://github.com/breatheco-de/python-flask-api-tutorial), it's a similar process, but instead of `tasks`, here you will be dealing with `people` and `planets`.

**👉 Please follow these steps on** [how to start a coding project](https://4geeks.com/lesson/how-to-start-a-project).

> 💡 Important: Remember to save and upload your code to GitHub by creating a new repository, updating the remote (`git remote set-url origin <your new url>`), and uploading the code to your new repository using the `add`, `commit` and `push` commands from the git terminal.

</onlyfor>

## 📝 Instructions

Create an API that connects to a database and implements the following endpoints (very similar to SWAPI.dev or SWAPI.tech):

- `[GET] /people` Get a list of all the people in the database.
- `[GET] /people/<int:people_id>` Get one single person's information.
- `[GET] /planets` Get a list of all the planets in the database.
- `[GET] /planets/<int:planet_id>` Get one single planet's information.

Additionally, create the following endpoints to allow your StarWars blog to have users and favorites:

- `[GET] /users` Get a list of all the blog post users.
- `[GET] /users/favorites` Get all the favorites that belong to the current user.
- `[POST] /favorite/planet/<int:planet_id>` Add a new favorite `planet` to the current user with the planet id = `planet_id`.
- `[POST] /favorite/people/<int:people_id>` Add new favorite `people` to the current user with the people id = `people_id`.
- `[DELETE] /favorite/planet/<int:planet_id>` Delete a favorite `planet` with the id = `planet_id`.
- `[DELETE] /favorite/people/<int:people_id>` Delete a favorite `people` with the id = `people_id`.
- Your current API does not have an authentication system (yet), which is why the only way to create users is directly on the database using the Flask admin.

> Note: here is a sample API in Postman: https://documenter.getpostman.com/view/2432393/TzRSgnTS#a4174b48-3fc8-46e3-bf82-19a08107666f

## 📖 Fundamentals

This exercise will make you practice the following fundamentals:

1. Building an RESTful API using one of the most popular libraries, [Python Flask](https://flask.palletsprojects.com/en/1.1.x/) or [Express.js](https://expressjs.com/).
2. Building a database with the **ORM** called [SQLAlchemy](https://www.sqlalchemy.org/) or [TypeORM](https://typeorm.io/)
3. Database Migrations using the migration system [Alembic](https://alembic.sqlalchemy.org/en/latest/) or the native migration system from TypeORM.

## 😎 Feeling confident?

The following requirements are not necessary to successfully complete this project, but you would like to try coding them if you feel like challenging yourself ☺️

`+4` Create also endpoints to add (POST), update (PUT), and delete (DELETE) planets and people. That way all the database information can be managed using the API instead of having to rely on the Flask admin to create the planets and people.

This and many other projects are built by students as part of the 4Geeks Academy [Coding Bootcamp](https://4geeksacademy.com/us/coding-bootcamp) by [Alejandro Sanchez](https://twitter.com/alesanchezr) and many other contributors. Find out more about our [Full Stack Developer Course](https://4geeksacademy.com/us/coding-bootcamps/part-time-full-stack-developer), and [Data Science Bootcamp](https://4geeksacademy.com/us/coding-bootcamps/datascience-machine-learning).
