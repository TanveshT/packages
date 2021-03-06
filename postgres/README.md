---
title: Postgres
homepage: https://www.postgresql.org/
tagline: |
  PostgreSQL: The World's Most Advanced Open Source Relational Database.
---

## Updating `postgres`

```bash
webi postgres@stable
```

Use `@x.y.z` for a specific version.

## Cheat Sheet

> Postgres is the all-in-one database for beginners and experts alike. It
> handles SQL, 'NoSQL', JSON, HSTORE, Full-Text Search, Messages Queues and
> more. Best bang for buck.

### Initialize a database with a password

```bash
echo "postgres" > /tmp/pwfile
mkdir -p $HOME/.local/share/postgres/var/

initdb -D $HOME/.local/share/postgres/var/ \
    --username postgres --pwfile "/tmp/pwfile" \
    --auth-local=password --auth-host=password

rm /tmp/pwfile
```

### Start the postgres server

```bash
postgres -D $HOME/.local/share/postgres/var -p 5432
```

### Connect with the psql client

```bash
psql 'postgres://postgres:postgres@localhost:5432/postgres'
```
