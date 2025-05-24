# Portainer

This is the main management app for Docker apps, and should be the first Docker app to be started.

```bash
docker compose up -d
```

Navigate to `https://localhost:9443/`.

Upon landing, create account as instructed on-screen, and login.

For full control of docker apps through Portainer, it is recommended to copy paste the individual `docker-compose.yaml` files into `Stacks` -> `+ Add Stack`. Otherwise the `Control` column for that container will be `Limited`.
