# postgres-docker-template

## Set Up
1. Change environment variables in `docker-compose.yml`
2. Run:
```bash
docker compose up -d
```

## Accessing PSQL through the container

```bash
sudo docker exec -it postgres_db psql -U postgres1 -d my_database
```

## Accessing pgAdmin
1. Open your web browser and navigate to http://localhost:8080 (or the port you mapped for pgAdmin).
2. Log in using the credentials you set in the docker-compose.yml (PGADMIN_DEFAULT_EMAIL and PGADMIN_DEFAULT_PASSWORD).
3. Once inside pgAdmin, click on Add New Server.
4. In the General tab, give the connection a name (e.g., "Postgres DB").
5. In the Connection tab, enter the following:

    Host: postgres (or localhost if you're accessing from the host machine).
    Port: 5432.
    Username: yourusername (same as POSTGRES_USER).
    Password: The POSTGRES_PASSWORD.

Save and connect.
