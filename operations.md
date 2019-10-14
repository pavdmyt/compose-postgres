# Initial setup

Run docker-compose:

```bash
# cd to the proper dir
$ docker-compose up -d
```

Create the DB:

```bash
# go inside postgres container
$ docker exec -ti postgres bash

# inside the container
$ psql -U postgres
postgres=# CREATE DATABASE mytestdb;
CREATE DATABASE
postgres=#\q
```

- Go to pgAdmin UI (in browser: `localhost:5050`)
- Login using `PGADMIN_DEFAULT_EMAIL` and `PGADMIN_DEFAULT_PASSWORD`
- Create the connection to postgres server:
  1. Servers -> Create -> Server
  2. Give random name (e.g. `local-pg`)
  3. At "Connection" tab: `Host name: postgres`, `Port: 5432`


### Reference

- https://medium.com/better-programming/connect-from-local-machine-to-postgresql-docker-container-f785f00461a7
