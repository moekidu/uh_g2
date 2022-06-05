# uh_g2
Grupo 2 UH Desarrollo de Aplicaciones

CREACION API

Instalar Docker > 
	sudo apt install docker.io

Instalar Postgres > 
	sudo docker pull postgres

Creacion instancia Postgres en Docker > 
	sudo docker run --name local-postgres -e POSTGRES_PASSWORD=root -d -p 5432:5432 postgres

Ver status de instancia > 
	sudo docker ps

	Ejemplo:

	CONTAINER ID   IMAGE      COMMAND                  CREATED          STATUS          PORTS                                       NAMES
	cf6940e9b41a   postgres   "docker-entrypoint.s…"   13 seconds ago   Up 12 seconds   0.0.0.0:5432->5432/tcp, :::5432->5432/tcp   local-postgres

Accesar contenedor docker (usar Container ID especifico en cada caso)> 
	sudo docker exec -it cf69 bash

Accesar Postgres con usuario por defecto >
  psql -U postgres << enter psql

Creacion de base de datos en Postgres >
  CREATE DATABASE api;

  Comandos dentro de Postgres >
  
  Ver estado de conexion:
  \conninfo
  
  Ver bases de datos:
  \list
  
  Ver roles:
  \du
  
  Salir de Postgre:
  \q
  
  Conectarse a base de datos api:
  \c api
