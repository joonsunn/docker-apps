# Docker Apps Using Docker Compose

To launch an app, `cd` into the relevant app folder and run:

```bash
docker compose up -d
```

To stop an app,

```bash
docker compose stop
```

To delete the container

```bash
docker compose down -v
```

Options to reclaim space from docker cache:

1. Clear builder cache (use this most of the time unless more space is needed):

   ```bash
   docker builder prune
   ```

2. Clear unused image:

   ```bash
   docker image prune
   ```

3. Clear stopped containers:

   ```bash
   docker container prune
   ```

4. Nuclear option:

   ```bash
   docker system prune
   ```

## Portainer

Navigate to `https://localhost:9443/`.

Upon landing, create account as instructed on-screen, and login.

For full control of docker apps through Portainer, it is recommended to copy paste the individual `docker-compose.yaml` files into `Stacks` -> `+ Add Stack`

## Postgres + PgAdmin

Navigate to `http://localhost:8080/`

By default, the Postgres container is running using the name `db`. So to connect to it on PgAdmin, use the following info:

```props
hostname: db
username: postgres
password: password
```

### Typical connection string

`postgresql://postgres:password@localhost:5432/postgres?schema=public`
