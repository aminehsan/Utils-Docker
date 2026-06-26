# Postgres

## How to run
```bash
psql -U admin
# or
psql -h localhost -p 5432 -U <owner> -d <database>
```

### Create User
```bash
CREATE USER <user> PASSWORD 'pass';
```

### Create Database
```bash
CREATE DATABASE <database_name>
WITH
  OWNER = "admin"
  TEMPLATE = "template0"
  ENCODING = 'UTF8'
  LC_COLLATE = 'C.UTF-8'
  LC_CTYPE = 'C.UTF-8'
  TABLESPACE = "pg_default";
```
