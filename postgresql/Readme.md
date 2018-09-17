- Run a postgresql: `docker run -p 5432:5432 --name some-postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgres`

- Access postgresql: `psql -U postgres -W -h 127.0.0.1`
