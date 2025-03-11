# Setup Postgresql
1. Note, if there is postgres on your computer/device, port 5432 is already in use. Therefore, replace the port other than 5432 (for example; 5433)
2. In `docker-compose.yml`, provide `port` value like this `port : “new_port:5432`

# Metabase Setup
1. In `docker-compose.yml`, `host_db_port` is `5432`, unless outside of docker. As DBeaver will open the postgre database in docker. We will direct our DBeaver to use the `new_port` port
1. Host database because it is in local docker, then use the host name `host.docker.internal`
