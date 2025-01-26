
# Sistema de RRHH de control - Docker Compose

Este es un proyecto que incluye dos submódulos, uno para el **frontend** y otro para el **backend**, y está orquestado con **Docker Compose** para facilitar su ejecución.

## Repositorios

- **Frontend**: Este repositorio contiene el código para la aplicación frontend, desarrollada con **React** y **TypeScript**. Puedes encontrar el repositorio aquí: [Frontend Repo](<https://github.com/esosa2/rrhh-control-fe>)
- **Backend**: Este repositorio contiene la API backend, desarrollada con **Node.js**, **Express** y **TypeScript**. Puedes encontrar el repositorio aquí: [Backend Repo](<https://github.com/esosa2/rrhh-control-be>)

Ambos proyectos se gestionan como submódulos dentro de este repositorio, lo que facilita su integración y ejecución conjunta.

## Clonar el Repositorio

Para clonar este proyecto y sus submódulos, utiliza el siguiente comando:

```bash
git clone --recurse-submodules https://github.com/esosa2/rrhh-control-funcionarios.git
```

Si ya has clonado el repositorio sin los submódulos, puedes inicializarlos y actualizarlos con:

```bash
git submodule update --init --recursive
```

Esto descargará el código tanto del **frontend** como del **backend**.

## Ejecutar con Docker

Una vez que hayas clonado el repositorio y actualizado los submódulos, puedes ejecutar el proyecto con Docker Compose utilizando el siguiente comando:

```bash
docker-compose up --build
```

Este comando construirá las imágenes necesarias y levantará los contenedores para el **frontend** y **backend**.

- **Frontend** estará disponible en `http://localhost:3000`.
- **Backend** estará disponible en `http://localhost:8001`.

## Detener los Contenedores

Para detener los contenedores, puedes usar:

```bash
docker-compose down
```

Este comando detendrá y eliminará los contenedores, redes y volúmenes creados por Docker Compose.

---

Este proyecto ya está listo para ejecutarse, solo debes seguir los pasos para clonar y levantar los contenedores. ¡Todo lo demás está configurado dentro del `docker-compose.yml`!
