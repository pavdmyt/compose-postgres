## Start postgres + pgAdmin

1. Go to config directory: `$ cd ~/git_cloned/compose-postgres`
2. Run containers: `$ docker-compose up -d`

**Optionally**: check that containers are up and running:

```bash
$ docker ps
CONTAINER ID        IMAGE                COMMAND                  CREATED             STATUS              PORTS                           NAMES
42f69056e268        postgres:12-alpine   "docker-entrypoint.s…"   4 seconds ago       Up 2 seconds        0.0.0.0:5432->5432/tcp          postgres
2726382dec4e        dpage/pgadmin4       "/entrypoint.sh"         4 seconds ago       Up 2 seconds        443/tcp, 0.0.0.0:5050->80/tcp   pgadmin
```

## pgAdmin usage

1. Once `postgres` and `pgadmin` containers are up and running, go to http://localhost:5050
2. At login page (if you're using Firefox) credentials should already be filled
3. After logged in, click at "Servers" at the leftside panel and find `mytestdb`
   under "Databases"
4. To run a SQL query against DB, choose desired DB at the leftside paben and
   click "Tools" -> "Query Tool" at pgAdmin's top bar
5. For all other questions on pgAdmin usage please refer to
   [docs](https://www.pgadmin.org/docs/pgadmin4/4.13/index.html)


## Stop postgres + pgAdmin

Simply run: `$ docker-compose stop`
(you should be inside `~/git_cloned/compose-postgres`)

