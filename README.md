# Docker Database Suite

This repository contains Docker Compose configurations for running multiple database systems and their management tools in Docker containers.

## Databases Included

- **PostgreSQL** with pgAdmin 4
- **MySQL** with phpMyAdmin
- **Microsoft SQL Server**
- **MongoDB** with Mongo Express

## How to Use

### Running All Databases

To start all database services:

```bash
docker-compose up -d
```

To stop all services:

```bash
docker-compose down
```

### Running Individual Databases

You can also run each database system separately by navigating to their respective folders:

```bash
# For PostgreSQL
cd postgre-compose
docker-compose up -d

# For MySQL
cd mysql-compose
docker-compose up -d

# For SQL Server
cd mssql-compose
docker-compose up -d

# For MongoDB
cd mongo-compose
docker-compose up -d
```

## Connection Information

### PostgreSQL
- **Host**: localhost
- **Port**: 5432
- **Username**: postgres
- **Password**: postgres
- **Admin Tool**: pgAdmin at http://localhost:5050

### MySQL
- **Host**: localhost
- **Port**: 3306
- **Root Username**: root
- **Root Password**: abcd@1234
- **Default Database**: mydb
- **Admin Tool**: phpMyAdmin at http://localhost:8080

### Microsoft SQL Server
- **Host**: localhost
- **Port**: 1433
- **Username**: sa
- **Password**: abcd@1234

### MongoDB
- **Host**: localhost
- **Port**: 27017
- **Admin Username**: root
- **Admin Password**: PassWord
- **Admin Tool**: Mongo Express at http://localhost:8081
