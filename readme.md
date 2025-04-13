# **PostgreSQL Setup**
1. If PostgreSQL is already installed on your machine, port 5432 is likely occupied. In that case, choose an alternative port, such as 5433.

2. In your `docker-compose.yml` file, map the port like this: `ports: "your_custom_port:5432"`.

# **Metabase Setup**
1. The default `host_db_port` in `docker-compose.yml` is set to `5432`, unless you're running Metabase outside Docker. Since DBeaver will connect to the PostgreSQL instance inside the Docker container, make sure to connect using the custom port you defined earlier.

2. Because the database is hosted locally within Docker, use `host.docker.internal` as the hostname when connecting.
