# PostgreSQL & pgAdmin4 Docker Compose
This is a simple docker-compose file to run a PostgreSQL database and pgAdmin4 web interface.

## Requirements
- Docker
- Docker Compose
- Internet connection (to download the images)
- A browser to access pgAdmin4
- A text editor to edit the environment variables
- A terminal to run the commands
- Basic knowledge of Docker and Docker Compose
- Basic knowledge of PostgreSQL
- Basic knowledge of pgAdmin4
- Basic knowledge of SQL
- Basic knowledge of Linux commands
- Basic knowledge of Git

## Installation
1. Clone this repository
2. Edit the environment variables in the `.env` file
3. Run the `docker-compose up -d` command
4. Access the pgAdmin4 web interface in your browser
5. Add a new server in pgAdmin4
6. Connect to the PostgreSQL database
7. Run SQL queries in the pgAdmin4 query tool
8. Stop the containers with the `docker-compose down` command
9. Start the containers with the `docker-compose up -d` command
10. Remove the containers with the `docker-compose down -v` command
11. Remove the volumes with the `docker volume prune` command
12. Remove the images with the `docker image prune` command
13. Remove the networks with the `docker network prune` command
14. Remove the dangling images with the `docker image prune` command
    
## Environment Variables
- `POSTGRES_USER`: The username for the PostgreSQL database (default: postgres)
- `POSTGRES_PASSWORD`: The password for the PostgreSQL database (default: postgres)
- `POSTGRES_DB`: The name of the PostgreSQL database (default: postgres)
- `PGADMIN_DEFAULT_EMAIL`: The email for the pgAdmin4 web interface (default:
- `PGADMIN_DEFAULT_PASSWORD`: The password for the pgAdmin4 web interface (default: postgres)
- `PGADMIN_LISTEN_PORT`: The port for the pgAdmin4 web interface (default: 5050)

## Access Information
- PostgreSQL database: `localhost:5432`
- pgAdmin4 web interface: `localhost:5050`
- Username: `congdinh2008@postgresql.com` (default)
- Password: `postgres` (default)
- Database: `postgres` (default)
- Host: `postgresql` (default)
- Port: `5432` (default)

