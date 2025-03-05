# MySQL and phpMyAdmin Docker Compose
This is a simple docker-compose file to run a MySQL database and phpMyAdmin web interface.

## Requirements
- Docker
- Docker Compose
- Internet connection (to download the images)
- A terminal to run the commands
- Basic knowledge of Docker and Docker Compose
- Basic knowledge of MySQL
- Basic knowledge of phpMyAdmin
- Basic knowledge of SQL
- Basic knowledge of Linux commands
- Basic knowledge of Git

## Installation
1. Clone this repository
2. Edit the environment variables in the `.env` file
3. Run the `docker-compose up -d` command
4. Access the phpMyAdmin web interface in your browser
5. Connect to the MySQL database
6. Run SQL queries in the phpMyAdmin query tool
7. Stop the containers with the `docker-compose down` command
8. Start the containers with the `docker-compose up -d` command
9. Remove the containers with the `docker-compose down -v` command
10. Remove the volumes with the `docker volume prune` command
11. Remove the images with the `docker image prune` command
12. Remove the networks with the `docker network prune` command
13. Remove the dangling images with the `docker image prune` command
    
## Environment Variables
- `MYSQL_ROOT_PASSWORD`: The password for the MySQL root user (default: root)
- `MYSQL_DATABASE`: The name of the MySQL database (default: mysql)
- `MYSQL_USER`: The username for the MySQL database (default: mysql)
- `MYSQL_PASSWORD`: The password for the MySQL database (default: mysql)
- `PHPMYADMIN_USERNAME`: The username for the phpMyAdmin web interface (default: admin)
- `PHPMYADMIN_PASSWORD`: The password for the phpMyAdmin web interface (default: admin)
- `PHPMYADMIN_PORT`: The port for the phpMyAdmin web interface (default: 8080)

## Access Information
- MySQL database: `localhost:3306`
- phpMyAdmin web interface: `localhost:8080`
- Username: `admin` (default)
- Password: `admin` (default)
- Database: `mysql` (default)
- Host: `mysql` (default)
- Port: `3306` (default)