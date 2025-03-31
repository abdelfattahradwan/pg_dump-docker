# pg_dump-minimal

Minimal Docker image containing only the PostgreSQL pg_dump utility without the full PostgreSQL installation.

## Usage

```bash
# Basic backup
docker run --rm abdelfattahradwan/pg_dump:17 -h host -U username -d dbname > backup.sql

# With password
docker run --rm -e PGPASSWORD=secret abdelfattahradwan/pg_dump:17 -h host -U username -d dbname > backup.sql

# Custom format (compressed)
docker run --rm -e PGPASSWORD=secret abdelfattahradwan/pg_dump:17 -h host -U username -d dbname -Fc > backup.dump
```

## Versions

Image tags follow PostgreSQL versions:

- 17: PostgreSQL 17

## Build

```bash
docker build -t pg_dump-minimal .
```

## Licence

MIT
