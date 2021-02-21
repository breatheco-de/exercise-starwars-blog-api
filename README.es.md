# ![alt text](https://assets.breatheco.de/apis/img/images.php?blob&random&cat=icon&tags=breathecode,32) StarWars Blog API

Es recomendad desarrollar este project en conjunto con el [StarWrs Blog Reading List](https://github.com/breatheco-de/exercise-starwars-blog-reading-list), eventualmente ese Front-End se integrará con el API que vas a desarrollar en este proyecto y tendrás una aplicación completamente funcional con Front-End y Back-End.

Hoy vamos a construir un API para administrar un blog (El Starwars Blog), los usuarios de este blog van a poder listar planetas, personas, y agregar o eliminer favoritos.

Para permitir que los usuarios hagan todo esto, debemos seguir los siguientes pasos:

1. Empieza por modelar una base de datos: Crea una base de datos y los modelos/tablas que van a contener esa informacion utilizando modelos de SQLAlchemy (tal vez esto ya lo tienes terminado si completaste este proyecto [StartWars DataModeling project](https://github.com/breatheco-de/exercise-starwars-data-modeling)).
2. Luego construye tus API Endpoints utilizando Flask, cada enpoint es una function que esta asociada a un URL y un metodo, por ejemplo `GET: /people`
3. En paralelo a la construción de tus endpoints debes ir probando que funcionen utilizando [Postman](https://www.postman.com/).

## 💻 Installation

Utiliza el bolerplate [Flask API boilerplate](https://github.com/4GeeksAcademy/flask-rest-hello) para empezar este proyecto, abrelo con Gitpod para eviar cualquier problema de configuracion local ya que utiliza una base de datos y python 3.7+ (todo eso ya viene instalado en Gitpod y tiende a ser engorroso de installar manualmente).

## 📝 Instructions

Crea un API conectada a una base de datos implemente las siguientes fuctionalidades (my similares a SWAPI.dev or SWAPI.tech):

- `[GET] /people` Get a list of all the people in the database
- `[GET] /planets` Get a list of all the planets in the database

Aditionally create the following endpoints to allow your StartWars blog to have users and favories:

- `[GET] /users` Get a list of all the blog post users (⚠️ Note: your blog users, this en)
- `[GET] /users/<int:user_id>/favorites` Get all the favorites that belong to the user with the id = `user_id`.
- `[POST] /users/<int:user_id>/favorites` Add a new favorite to the user with the id = `user_id`.
- `[DELETE] /favorite/<int:favorite_id>` Delete favorite with the id = `favorite_id`.

Your current API does not have an authentication system (yet), that is why the only at to create users is directly on the database using the flask admin.

## 📖 Fundamentals

This exercise will make you practice the following fundamentals:

1. Building an RESTful API.
2. Building a database with SQLAlchemy.
3. Database Migrations.

## 😎 Feeling confident?

`+1` Create also an enpoint to add (POST), update (PUT), and delete (DELETE) planets and people, that way all the database information can be manage using the API instead of having to rely on the flask admin to create the plantes and people.