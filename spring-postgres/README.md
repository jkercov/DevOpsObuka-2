## Compose sample application

### Use with Docker Development Environments

You can open this sample in the Dev Environments feature of Docker Desktop version 4.12 or later.

[Open in Docker Dev Environments <img src="../open_in_new.svg" alt="Open in Docker Dev Environments" align="top"/>](https://open.docker.com/dashboard/dev-envs?url=https://github.com/docker/awesome-compose/tree/master/spring-postgres)

### Java application with Spring framework and a Postgres database

Project structure:
```
.
├── backend
│   ├── Dockerfile
│   └── ...
├── compose.yaml
└── README.md

```

[_compose.yaml_](compose.yaml)
```
The compose file defines an application with two services `backend` and `db`.
When deploying the application, docker compose maps port 8080 of the backend service container to port 8080 of the host as specified in the file.
Make sure port 8080 on the host is not already being in use.

For `db` use PostgreSQL and db called example
```
Create volume for db with name db-data and path /var/lib/postgresql/data

## Deploy with docker compose

```
$ docker compose up -d

WARNING: Image for service backend was built because it did not already exist. To rebuild this image you must use `docker-compose build` or `docker-compose up --build`.
```

## Expected result

Listing containers must show two containers running and the port mapping as below:
```
$ docker ps
```

