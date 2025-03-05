# Microsoft SQL Server Docker Compose
This is a simple docker-compose configuration to run a Microsoft SQL Server database.

## Requirements
- Docker
- Docker Compose
- Internet connection (to download the images)
- A terminal to run the commands
- Basic knowledge of Docker and Docker Compose
- Basic knowledge of Microsoft SQL Server
- Basic knowledge of T-SQL
- Basic knowledge of Linux/macOS commands

## Installation
1. Clone this repository
2. Edit the environment variables in the `.env` file
3. Run the `docker-compose up -d` command
4. Connect to the MS SQL Server using a client like:
   - Azure Data Studio
   - SQL Server Management Studio (SSMS)
   - Visual Studio Code with SQL Server extension
   - Command line with sqlcmd utility
5. Run SQL queries using your preferred client
6. Stop the containers with the `docker-compose down` command
7. Start the containers with the `docker-compose up -d` command
8. Remove the containers with the `docker-compose down -v` command
9. Remove the volumes with the `docker volume prune` command

## Environment Variables
- `MSSQL_SA_PASSWORD`: The password for the MS SQL Server sa user (change it from default!)
- `ACCEPT_EULA=Y`: Required to accept Microsoft's End-User License Agreement

## Access Information
- MS SQL Server: `localhost:1433`
- Username: `sa` (default system admin)
- Password: as defined in your `.env` file
- Authentication: SQL Server Authentication

## Connection String Examples
### .NET / C#
```csharp
"Server=localhost,1433;Database=master;User Id=sa;Password=yourPassword;TrustServerCertificate=True;"
```

### JDBC (Java)
```
jdbc:sqlserver://localhost:1433;databaseName=master;user=sa;password=yourPassword;encrypt=true;trustServerCertificate=true;
```

### Node.js (with mssql)
```javascript
{
  user: 'sa',
  password: 'yourPassword',
  server: 'localhost',
  port: 1433,
  database: 'master',
  options: {
    encrypt: true,
    trustServerCertificate: true
  }
}
```

### Python (with pyodbc)
```python
"DRIVER={ODBC Driver 18 for SQL Server};SERVER=localhost,1433;DATABASE=master;UID=sa;PWD=yourPassword;TrustServerCertificate=yes;"
```

## Notes
- The default image uses the 2022 version of SQL Server
- Data is persisted in a Docker volume named `sqlvolume`
- The password must meet SQL Server's complexity requirements (at least 8 characters long with uppercase, lowercase, numbers and special characters)
