# RRHH Control - Setup con Docker Compose

Este repositorio contiene los submódulos necesarios para levantar un sistema de control de RRHH que incluye frontend, backend y base de datos. Aquí encontrarás los pasos para clonar, configurar y ejecutar el proyecto utilizando Docker Compose.

## Requisitos Previos

1. Tener instalado [Docker](https://www.docker.com/) y [Docker Compose](https://docs.docker.com/compose/).
2. Tener configurado Git en tu máquina local.

## Pasos de Configuración

### 1. Clonar el repositorio principal
Clona este repositorio utilizando el siguiente comando:

```bash
git clone --recurse-submodules <URL_DEL_REPOSITORIO>
```

Si ya has clonado el repositorio y necesitas actualizar los submódulos, utiliza:

```bash
git submodule update --init --recursive
```

### 2. Configurar archivos necesarios
Asegúrate de que los submódulos `frontend` y `backend` contienen sus respectivos `Dockerfile` correctamente configurados.

Si necesitas realizar cambios, asegúrate de volver a construir las imágenes con el comando que aparece en el paso

### 3. Construir y levantar los servicios
Ejecuta el siguiente comando en la raíz del proyecto para construir las imágenes y levantar los servicios:

```bash
docker compose up --build
```

Esto levantará los servicios en los siguientes puertos predeterminados:
- Frontend: [http://localhost:3000](http://localhost:3000)
- Backend: [http://localhost:8001](http://localhost:8001)
- Base de datos (PostgreSQL): puerto 5432

### 4. Detener los servicios
Para detener y eliminar los contenedores (sin afectar los datos persistentes), utiliza:

```bash
docker compose down
```

Si deseas eliminar los contenedores, redes y volúmenes asociados:

```bash
docker compose down -v
```


