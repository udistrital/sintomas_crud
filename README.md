# evaluaciones_mongo_crud

API CRUD para el registro de estado de salud diario para el cliente de alternancia 

## Especificaciones Técnicas

### Tecnologías Implementadas y Versiones
* [NestJS](https://github.com/nestjs/nest)
* [MongoDB](https://github.com/mongodb/mongo)
* [Docker](https://docs.docker.com/engine/install/ubuntu/)
* [Docker Compose](https://docs.docker.com/compose/)

### Variables de Entorno
```shell
SINTOMAS_CRUD_USER=[Usuario de BD]
SINTOMAS_CRUD_PASS=[Contraseña del usuario de BD]
SINTOMAS_CRUD_HOST=[URL, Dominio o EndPoint de la BD]
SINTOMAS_CRUD_PORT=[Puerto de la BD]
SINTOMAS_CRUD_DB=[Nombre de Base de Datos]
SINTOMAS_CRUD_DB=[Nombre de Base de Datos de Autenticación]
SINTOMAS_CRUD_HTTP_PORT=[Puerto de exposición del API]
```
**NOTA:** Las variables se pueden ver en el fichero conf/app.conf y están identificadas con SINTOMAS_CRUD...

### Ejecución del Proyecto
```shell
#1. Obtener el repositorio con nest
git clone https://github.com/udistrital/sintomas_crud

#2. Moverse a la carpeta del repositorio
cd sintomas_crud

# 3. Moverse a la rama **develop**
git pull origin develop && git checkout develop

4. Instalar dependencias
npm install 
#o
npm i

# 5. Alimentar todas las variables de entorno que utiliza el proyecto.
SINTOMAS_CRUD_HTTP_PORT=8080 
SINTOMAS_CRUD_HOST=127.0.0.1:27017 SINTOMAS_CRUD_SOME_VARIABLE=some_value nest run
```
### Ejecución Dockerfile
```shell
# docker build --tag=sintomas_crud . --no-cache
# docker run -p 80:80 sintomas_crud
```

### Ejecución docker-compose
```shell
#1. Clonar el repositorio
git clone -b develop https://github.com/udistrital/sintomas_crud

#2. Moverse a la carpeta del repositorio
cd sintomas_crud

#3. Crear un fichero con el nombre **custom.env**
touch custom.env

#4. Crear la network **back_end** para los contenedores
docker network create back_end

#5. Ejecutar el compose del contenedor
docker-compose up --build

#6. Comprobar que los contenedores estén en ejecución
docker ps
```

### Ejecución Pruebas

Pruebas unitarias
```shell
# En Proceso
```

## Modelo de Datos
[Modelo de Datos Parametros](/database/sintomas_crud.png)

## Estado CI

| Develop | Relese 0.0.1 | Master |
| -- | -- | -- |
| [![Build Status](https://hubci.portaloas.udistrital.edu.co/api/badges/udistrital/sintomas_crud/status.svg?ref=refs/heads/develop)](https://hubci.portaloas.udistrital.edu.co/udistrital/sintomas_crud) | [![Build Status](https://hubci.portaloas.udistrital.edu.co/api/badges/udistrital/sintomas_crud/status.svg?ref=refs/heads/release/0.0.1)](https://hubci.portaloas.udistrital.edu.co/udistrital/sintomas_crud) |  [![Build Status](https://hubci.portaloas.udistrital.edu.co/api/badges/udistrital/sintomas_crud/status.svg)](https://hubci.portaloas.udistrital.edu.co/udistrital/sintomas_crud) |


## Licencia

This file is part of sintomas_crud.

sintomas_crud is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

sintomas_crud is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with sintomas_crud. If not, see https://www.gnu.org/licenses/.
