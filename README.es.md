# ![alt text](https://assets.breatheco.de/apis/img/images.php?blob&random&cat=icon&tags=breathecode,32) StarWars Blog API

Es recomendado desarrollar este project en conjunto con el [StarWars Blog Reading List](https://github.com/breatheco-de/exercise-starwars-blog-reading-list), eventualmente ese Front-End se integrará con el API que vas a desarrollar en este proyecto y tendrás una aplicación completamente funcional con Front-End y Back-End.

Hoy vamos a construir un API para administrar un blog (El Starwars Blog), los usuarios de este blog van a poder listar planetas, personas, y agregar o eliminar favoritos.

Para permitir que los usuarios hagan todo esto, debemos seguir los siguientes pasos:

1. Comienza por modelar la base de datos: crea una base de datos y las tablas necesarias para almacenar esa información, es posible que ya lo hayas hecho en el proyecto StartWars DataModeling en [python/flask](https://github.com/breatheco-de/exercise-starwars-data-modeling) o [node/express](https://github.com/breatheco-de/starwars-data-model-typeorm-node)
2. Crea tus endpoints finales utilizando Flask o Express (según el idioma principal de tu clase).
3. Prueba constantemente endpoints con Postman.

## 🌱  Cómo iniciar este proyecto

No clones este repositorio.

El primer paso para comenzar a codificar es clonar el [flask boilerplate](https://github.com/4GeeksAcademy/flask-rest-hello) o el [express.js boilerplate](https://github.com/breatheco-de/starwars-data-model-typeorm-node), esto dependerá del principal lenguaje de backend de tu clase.

a) Si usas Gitpod (recomendado) puedes clonar el boilerplate de **python**[haciendo clic aquí](https://github.com/4GeeksAcademy/flask-rest-hello) or el boilerplate de **node.js** [haciendo clic aquí](https://github.com/4GeeksAcademy/expressjs-rest-hello).

b) Si trabajas localmente, escribe el siguiente comando en tu terminal: 
```sh
Para Python/Flask:
$ git clone https://github.com/4GeeksAcademy/flask-rest-hello

Para Node/Express.js:
$ git clone https://github.com/4GeeksAcademy/expressjs-rest-hello
```
(si trabajas localmente debees tener una base de datos y python 3.7+ pero puedes usar Gitpod, trae todo instalado)

🐍 Para Python:El boilerplate tiene un archivo README con instrucciones y un video de como usarlo y como construir un API. Puedes hacer este tutorial interactivo primero sobre [como construir API's con Flask](https://github.com/breatheco-de/python-flask-api-tutorial).

💡 Importante: Recuerda actualizar el `remote` del proyecto con el de tu repositorio usando `git remote set-url origin <your new url>`, y luego guardar tu código en tu nuevo repositorio usando `add`, `commit` y `push`.

## 📝 Instructiones

Crea un API conectada a una base de datos e implemente los siguientes endpoints (my similares a SWAPI.dev or SWAPI.tech):

- `[GET] /people` Listar todos los registros de `people` en la base de datos
- `[GET] /people/<int:people_id>` Listar la información de una sola `people`
- `[GET] /planets` Listar los registros de `planets` en la base de datos
- `[GET] /planets/<int:planet_id>` Listar la información de un solo `planet`

Adicionalmente necesitamos crear los siguientes endpoints para que podamos tener usuarios en nuestro blog:

- `[GET] /users` Listar todos los usuarios del blog 
- `[GET] /users/favorites` Listar todos los favoritos que pertenecen al usuario actual.
- `[POST] /favorite/planet/<int:planet_id>` Añade un nuevo `planet`favorito al usuario actual con el planet id = `planet_id`.
- `[POST] /favorite/people/<int:planet_id>` Añade una nueva `people`favorita al usuario actual con el people.id = `people_id`.
- `[DELETE] /favorite/planet/<int:planet_id>` Elimina un `planet favorito con el id = planet_id`.
- `[DELETE] /favorite/people/<int:people_id>` Elimina una `people`faorita con el id = `people_id`.
- Tu API actual no tiene un sistema de autenticación (todavía), es por eso que la única forma de crear usuarios es directamente en la base de datos usando el flask admin.

☝️ Nota: Aquí hay un ejemplo en Postman: 
https://documenter.getpostman.com/view/2432393/TzRSgnTS#a4174b48-3fc8-46e3-bf82-19a08107666f

## 📖 Fundamentos

Este ejercicio te permitira practicar las siguientes habilidades y conceptos:

1. Construcción de API's utilizanod el standard REST (A.k.a: RESTful API's)
2. Construir una base de datos utilizando el **ORM** llamado [SQLAlchemy](https://www.sqlalchemy.org/).
3. Utilizar y entender sistemas de migraciones de bases de datos con [Alembic](https://alembic.sqlalchemy.org/en/latest/).

## 😎 Te sientes con confianza?

Los siguients requerimientos no son necesarios para completar el projecto satisfactoriamente pero puedes desarrollarlos para continuar tu aprendizaje si te sientes con suficiente confianza.

`+4` Crea API Endpoints para agregar (POST), modificar (PUT) y eliminar (DELETE) `planets` y `people`. De esta manera toda la base de datos va a poder ser administrada via API.
