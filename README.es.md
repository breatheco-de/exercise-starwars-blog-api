# ![alt text](https://assets.breatheco.de/apis/img/images.php?blob&random&cat=icon&tags=breathecode,32) StarWars Blog API

Es recomendado desarrollar este project en conjunto con el [StarWars Blog Reading List](https://github.com/breatheco-de/exercise-starwars-blog-reading-list), eventualmente ese Front-End se integrará con el API que vas a desarrollar en este proyecto y tendrás una aplicación completamente funcional con Front-End y Back-End.

Hoy vamos a construir un API para administrar un blog (El Starwars Blog), los usuarios de este blog van a poder listar planetas, personas, y agregar o eliminer favoritos.

Para permitir que los usuarios hagan todo esto, debemos seguir los siguientes pasos:

1. Empieza por modelar una base de datos: Crea una base de datos y los modelos/tablas que van a contener esa informacion utilizando modelos de SQLAlchemy (tal vez esto ya lo tienes terminado si completaste este proyecto [StartWars DataModeling project](https://github.com/breatheco-de/exercise-starwars-data-modeling)).
2. Luego construye tus API Endpoints utilizando Flask, cada enpoint es una function que esta asociada a un URL y un metodo, por ejemplo `GET: /people`
3. En paralelo a la construción de tus endpoints debes ir probando que funcionen utilizando [Postman](https://www.postman.com/).

## 🌱  Cómo iniciar este proyecto

No clones este repositorio.

El primer paso para comenzar a codificar es clonar el [flask boilerplate](https://github.com/4GeeksAcademy/flask-rest-hello) en tu compjutador local o con Gitpod.

a) Si usas Gitpod puedes clonar el boilerplate [clic aquí](https://gitpod.io#https://github.com/4GeeksAcademy/flask-rest-hello).

b) Si trabajas localmente, escribe el siguiente comando en tu terminal: 
```sh
$ git clone https://gitpod.io#https://github.com/4GeeksAcademy/flask-rest-hello
```
(si trabajas localmente debees tener una base de datos y python 3.7+ pero puedes usar Gitpod, trae todo instalado)

El boilerplate tiene un archivo README con instrucciones y un video de como usarlo y como construir un API. Puedes hacer este tutorial interactivo primero sobre [como construir API's con Flask](https://github.com/breatheco-de/python-flask-api-tutorial).

💡 Importante: Recuerda actualizar el `remote` del proyecto con el de tu repositorio usando `git remote set-url origin <your new url>`, y luego guardar tu código en tu nuevo repositorio usando `add`, `commit` y `push`.

## 📝 Instructiones

Crea un API conectada a una base de datos implemente las siguientes fuctionalidades (my similares a SWAPI.dev or SWAPI.tech):

- `[GET] /people` Listar todos los registros de `people` in la base de datos
- `[GET] /planets` Listar los registros de `planets` en la base de datos

Adicionalmente necesitamos crear los siguientes endpoints para que podamos tener usuarios en nuestro blog:

- `[GET] /users` Listar todos los usuarios del blog
- `[GET] /users/<int:user_id>/favorites` Listar todos los `favorites` que pertenecen al usuario con el id = `user_id`.
- `[POST] /users/<int:user_id>/favorites` Agregar un nuevo favorito al usuario with the id = `user_id`.
- `[DELETE] /favorite/<int:favorite_id>` Eliminar un favorito de un usuario con el id = `favorite_id`.

El API no va a disponer de de un sistema de autenticación (por ahora), pero podemos crear usuarios directamente en la base de datos utizando el Flask admin: `https://url_de_tu_api/admin`



- Aun no te sientes con confianza? Empieza a programar y ve cometiendo errores, utiliza video tutoriales para apoyarte, asegurate de que los videos sean sobre construir API con Flask ya que Flask peude ser utilizar para construir website HTML tambien y eso no es lo que estamos haciendo en este proyecto.

## 📖 Fundamentos

Este ejercicio te permitira practicar las siguientes habilidades y conceptos:

1. Construcción de API's utilizanod el standard REST (A.k.a: RESTful API's)
2. Construir una base de datos utilizando el **ORM** llamado [SQLAlchemy](https://www.sqlalchemy.org/).
3. Utilizar y entender sistemas de migraciones de bases de datos con [Alembic](https://alembic.sqlalchemy.org/en/latest/).

## 😎 Te sientes con confianza?

Los siguients requerimientos no son necesarios para completar el projecto satisfactoriamente pero puedes desarrollarlos para continuar tu aprendizaje si te sientes con suficiente confianza.

`+4` Crea API Endpoints para agregar (POST), modificar (PUT) y eliminar (DELETE) `planets` y `people`. De esta manera toda la base de datos va a poder ser administrada via API.
