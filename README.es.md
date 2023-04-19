<!--hide-->
# StarWars Blog API
<!--endhide--> 

Es recomendado desarrollar este proyecto en conjunto con el [StarWars Blog Reading List](https://github.com/breatheco-de/exercise-starwars-blog-reading-list), eventualmente ese Front-End se integrará con el API que vas a desarrollar en este proyecto y tendrás una aplicación completamente funcional con Front-End y Back-End.

Hoy vamos a construir un API para administrar un blog (El Starwars Blog), los usuarios de este blog van a poder listar planetas, personas, y agregar o eliminar favoritos.

Para permitir que los usuarios hagan todo esto, debemos seguir los siguientes pasos:

1. Comienza por modelar la base de datos: crea una base de datos y las tablas necesarias para almacenar esa información, es posible que ya lo hayas hecho en el proyecto StartWars DataModeling en [python/flask](https://github.com/breatheco-de/exercise-starwars-data-modeling) o [node/express](https://github.com/breatheco-de/starwars-data-model-typeorm-node)
2. Crea tus endpoints finales utilizando Flask o Express (según el idioma principal de tu clase).
3. Prueba constantemente los endpoints con Postman.

## 🌱 Cómo comenzar este proyecto

No clones este repositorio porque vamos a usar una plantilla diferente.

Recomendamos abrir el `flask template` o el `express.js template` usando una herramienta de aprovisionamiento como [Codespaces](https://4geeks.com/es/lesson/tutorial-de-github-codespaces) (recomendado) o [Gitpod](https://4geeks.com/es/lesson/como-utilizar-gitpod). Alternativamente, puedes clonarlo en tu computadora local usando el comando `git clone`.

Estos son los repositorios que necesitas abrir o clonar:

```
🐍 Para Python/Flask:
https://github.com/4GeeksAcademy/flask-rest-hello

👩🏽‍💻 Para Node/Express.js:
https://github.com/4GeeksAcademy/expressjs-rest-hello
```

(si trabajas localmente debes tener una base de datos y Node.js o python 3.7+ pero puedes usar Gitpod, trae todo instalado)

🐍 Para Python: El boilerplate tiene un archivo README con instrucciones y un video de como usarlo y como construir un API. Puedes hacer este tutorial interactivo primero sobre [como construir API's con Flask](https://github.com/breatheco-de/python-flask-api-tutorial).

**👉 Por favor sigue estos pasos** [cómo comenzar un proyecto de codificación](https://4geeks.com/es/lesson/como-comenzar-un-proyecto-de-codificacion).

💡 Importante: Recuerda guardar y subir tu código a GitHub creando un nuevo repositorio, actualizando el remoto (`git remote set-url origin <your new url>`) y subiendo el código a tu nuevo repositorio usando los comandos `add`, `commit` y `push` desde la terminal de git.

## 📝 Instrucciones

Crea un API conectada a una base de datos e implemente los siguientes endpoints (muy similares a SWAPI.dev or SWAPI.tech):

- `[GET] /people` Listar todos los registros de `people` en la base de datos
- `[GET] /people/<int:people_id>` Listar la información de una sola `people`
- `[GET] /planets` Listar los registros de `planets` en la base de datos
- `[GET] /planets/<int:planet_id>` Listar la información de un solo `planet`

Adicionalmente, necesitamos crear los siguientes endpoints para que podamos tener usuarios en nuestro blog:

- `[GET] /users` Listar todos los usuarios del blog 
- `[GET] /users/favorites` Listar todos los favoritos que pertenecen al usuario actual.
- `[POST] /favorite/planet/<int:planet_id>` Añade un nuevo `planet` favorito al usuario actual con el planet id = `planet_id`.
- `[POST] /favorite/people/<int:people_id>` Añade una nueva `people` favorita al usuario actual con el people.id = `people_id`.
- `[DELETE] /favorite/planet/<int:planet_id>` Elimina un `planet` favorito con el id = planet_id`.
- `[DELETE] /favorite/people/<int:people_id>` Elimina una `people` favorita con el id = `people_id`.
- Tu API actual no tiene un sistema de autenticación (todavía), es por eso que la única forma de crear usuarios es directamente en la base de datos usando el flask admin.

☝️ Nota: Aquí hay un ejemplo en Postman: 
https://documenter.getpostman.com/view/2432393/TzRSgnTS#a4174b48-3fc8-46e3-bf82-19a08107666f

## 📖 Fundamentos

Este ejercicio te permitirá practicar las siguientes habilidades y conceptos:

1. Construcción de API's utilizando el standard REST (A.k.a: RESTful API's)
2. Construir una base de datos utilizando el **ORM** llamado [SQLAlchemy](https://www.sqlalchemy.org/) o TypeORM (https://typeorm.io/).
3. Utilizar y entender sistemas de migraciones de bases de datos con [Alembic](https://alembic.sqlalchemy.org/en/latest/) o las migraciones nativas de TypeORM (en el caso de node.js).

## 😎 Te sientes con confianza?

Los siguientes requerimientos no son necesarios para completar el proyecto satisfactoriamente, pero puedes desarrollarlos para continuar tu aprendizaje si te sientes con suficiente confianza.

`+4` Crea API Endpoints para agregar (POST), modificar (PUT) y eliminar (DELETE) `planets` y `people`. De esta manera, toda la base de datos va a poder ser administrada via API.

Este y otros proyectos son usados para [aprender a programar](https://4geeksacademy.com/es/aprender-a-programar/aprender-a-programar-desde-cero) por parte de los alumnos de 4Geeks Academy [Coding Bootcamp](https://4geeksacademy.com/us/coding-bootcamp) realizado por [Alejandro Sánchez](https://twitter.com/alesanchezr) y muchos otros contribuyentes. Conoce más sobre nuestros [Curso de Programación](https://4geeksacademy.com/es/curso-de-programacion-desde-cero?lang=es) para convertirte en [Full Stack Developer](https://4geeksacademy.com/es/coding-bootcamps/desarrollador-full-stack/?lang=es), o nuestro [Data Science Bootcamp](https://4geeksacademy.com/es/coding-bootcamps/curso-datascience-machine-learning).
