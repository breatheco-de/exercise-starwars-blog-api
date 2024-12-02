<!--hide-->
# StarWars Blog API
<!--endhide--> 

Es recomendado desarrollar este proyecto en conjunto con el [StarWars Blog Reading List](https://github.com/breatheco-de/exercise-starwars-blog-reading-list), eventualmente ese front-end se integrará con la API que vas a desarrollar en este proyecto y tendrás una aplicación completamente funcional con front-end y back-end.

Hoy vamos a construir una API para administrar un blog (El StarWars Blog), los usuarios de este blog van a poder listar planetas, personajes, y agregar o eliminar favoritos.

Para permitir que los usuarios hagan todo esto, debemos seguir los siguientes pasos:

1. Comienza por modelar la base de datos: crea una base de datos y las tablas necesarias para almacenar esa información, es posible que ya lo hayas hecho en el proyecto StarWars DataModeling en [python/flask](https://github.com/breatheco-de/exercise-starwars-data-modeling) o [node/express](https://github.com/breatheco-de/starwars-data-model-typeorm-node).
2. Crea tus endpoints utilizando Flask o Express (según el lenguaje principal de tu clase).
3. Prueba constantemente tus endpoints con [Postman](https://www.postman.com/).

<onlyfor saas="false" withBanner="false">
  
## 🌱 Cómo comenzar este proyecto

No clones este repositorio porque vamos a usar una plantilla diferente.

Recomendamos abrir el `flask template` o el `express.js template` usando un entorno de desarrollo como [Codespaces](https://4geeks.com/es/lesson/tutorial-de-github-codespaces) (recomendado) o [Gitpod](https://4geeks.com/es/lesson/como-utilizar-gitpod). Alternativamente, puedes clonarlo en tu computadora local usando el comando `git clone`.

Estos son los repositorios que necesitas abrir o clonar:

```text
🐍 Para Python/Flask:
https://github.com/4GeeksAcademy/flask-rest-hello

👩🏽‍💻 Para Node/Express.js:
https://github.com/4GeeksAcademy/expressjs-rest-hello
```

> ⚠ Si trabajas localmente debes tener una base de datos y Node.js o Python 3.7+ pero si usas Codespaces o Gitpod ya viene todo instalado.

🐍 Para Python: El boilerplate tiene un archivo README con instrucciones y un video de como usarlo y como construir una API. Puedes hacer este tutorial interactivo primero sobre [como construir APIs con Flask](https://github.com/breatheco-de/python-flask-api-tutorial).

**👉 Por favor sigue estos pasos sobre** [cómo comenzar un proyecto de programación](https://4geeks.com/es/lesson/como-comenzar-un-proyecto-de-codificacion).

> 💡 Importante: Recuerda guardar y subir tu código a GitHub creando un nuevo repositorio, actualizando el remoto (`git remote set-url origin <your new url>`) y subiendo el código a tu nuevo repositorio usando los comandos `add`, `commit` y `push` desde la terminal de git.

</onlyfor>

## 📝 Instrucciones

Crea una API conectada a una base de datos e implemente los siguientes endpoints (muy similares a SWAPI.dev or SWAPI.tech):

- `[GET] /people` Listar todos los registros de `people` en la base de datos.
- `[GET] /people/<int:people_id>` Muestra la información de un solo personaje según su id.
- `[GET] /planets` Listar todos los registros de `planets` en la base de datos.
- `[GET] /planets/<int:planet_id>` Muestra la información de un solo planeta según su id.

Adicionalmente, necesitamos crear los siguientes endpoints para que podamos tener usuarios y favoritos en nuestro blog:

- `[GET] /users` Listar todos los usuarios del blog.
- `[GET] /users/favorites` Listar todos los favoritos que pertenecen al usuario actual.
- `[POST] /favorite/planet/<int:planet_id>` Añade un nuevo `planet` favorito al usuario actual con el id = `planet_id`.
- `[POST] /favorite/people/<int:people_id>` Añade un nuevo `people` favorito al usuario actual con el id = `people_id`.
- `[DELETE] /favorite/planet/<int:planet_id>` Elimina un `planet` favorito con el id = `planet_id`.
- `[DELETE] /favorite/people/<int:people_id>` Elimina un `people` favorito con el id = `people_id`.
- Tu API actual no tiene un sistema de autenticación (todavía), es por eso que la única forma de crear usuarios es directamente en la base de datos usando el Flask admin.

> Nota: Aquí hay un ejemplo en Postman: https://documenter.getpostman.com/view/2432393/TzRSgnTS#a4174b48-3fc8-46e3-bf82-19a08107666f

## 📖 Fundamentos

Este ejercicio te permitirá practicar las siguientes habilidades y conceptos:

1. Construcción de APIs utilizando el standard REST (a.k.a: RESTful APIs).
2. Construir una base de datos utilizando el **ORM** llamado [SQLAlchemy](https://www.sqlalchemy.org/) o [TypeORM](https://typeorm.io/).
3. Utilizar y entender sistemas de migraciones de bases de datos con [Alembic](https://alembic.sqlalchemy.org/en/latest/) o las migraciones nativas de TypeORM (en el caso de node.js).

## 😎 Te sientes con confianza?

Los siguientes requerimientos no son necesarios para completar el proyecto satisfactoriamente, pero puedes desarrollarlos para continuar tu aprendizaje si te sientes con suficiente confianza.

`+4` Crea endpoints para agregar (POST), modificar (PUT) y eliminar (DELETE) `planets` y `people`. De esta manera, toda la base de datos va a poder ser administrada vía API en vez de depender del admin de Flask.

Este y otros proyectos son usados para [aprender a programar](https://4geeksacademy.com/es/aprender-a-programar/aprender-a-programar-desde-cero) por parte de los alumnos de 4Geeks Academy [Coding Bootcamp](https://4geeksacademy.com/us/coding-bootcamp) realizado por [Alejandro Sánchez](https://twitter.com/alesanchezr) y muchos otros contribuyentes. Conoce más sobre nuestros [Cursos de Programación](https://4geeksacademy.com/es/curso-de-programacion-desde-cero?lang=es) para convertirte en [Full Stack Developer](https://4geeksacademy.com/es/coding-bootcamps/desarrollador-full-stack/?lang=es), o nuestro [Data Science Bootcamp](https://4geeksacademy.com/es/coding-bootcamps/curso-datascience-machine-learning).
