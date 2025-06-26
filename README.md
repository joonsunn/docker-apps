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

## Setup

Start with Portainer, and preferabley add/manage containers/stacks through the Portainer interface.

## Port numbers at a glance

| Port number | App       |
| ----------- | --------- |
| 9443        | Portainer |
| 8080        | PgAdmin   |
| 5432        | Postgres  |

## Updating apps

Docker images receive updates periodically. To update the apps,

```bash
docker compose down
docker compose pull
docker compose up -d
```
