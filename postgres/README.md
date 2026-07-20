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

### Dump and Restore
```bash
pg_dump --host=<host> --port=<port> --username=<username> --dbname=<dbname> --file="./<name>.dump" --format=custom --no-owner --no-privileges --compress=9 --verbose
pg_restore --host=<host> --port=<port> --username=<username> --dbname=<dbname> --clean --if-exists --no-owner --verbose "./<name>.dump"
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
