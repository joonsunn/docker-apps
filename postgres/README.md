# Postgres + PgAdmin

Navigate to `http://localhost:8080/`

By default, the Postgres container is running using the name `db`. So to connect to it on PgAdmin, use the following info:

```props
hostname: db
username: postgres
password: password
```

## Typical connection string

`postgresql://postgres:password@localhost:5432/postgres?schema=public`
