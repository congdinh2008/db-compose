# MongoDB Docker Compose
This is a Docker Compose configuration to run MongoDB and mongo-express for database management.

## Requirements
- Docker
- Docker Compose
- Internet connection (to download the images)
- A terminal to run the commands
- Basic knowledge of Docker and Docker Compose
- Basic knowledge of MongoDB

## Installation
1. Clone this repository
2. Edit the environment variables in the `.env` file
3. Run the `docker-compose up -d` command
4. Access MongoDB using your preferred client:
   - MongoDB Compass
   - mongo shell
   - Programming language drivers
5. Access mongo-express web interface at `http://localhost:8081`
6. Stop the containers with the `docker-compose down` command
7. Start the containers with the `docker-compose up -d` command
8. Remove the containers with the `docker-compose down -v` command
9. Remove the volumes with the `docker volume prune` command

## Environment Variables
### MongoDB
- `MONGO_INITDB_ROOT_USERNAME`: Root admin username
- `MONGO_INITDB_ROOT_PASSWORD`: Root admin password
- `MONGO_INITDB_USERNAME`: Regular user username
- `MONGO_INITDB_PASSWORD`: Regular user password

### Mongo Express
- `ME_CONFIG_MONGODB_SERVER`: MongoDB server hostname
- `ME_CONFIG_MONGODB_PORT`: MongoDB port
- `ME_CONFIG_MONGODB_ENABLE_ADMIN`: Enable admin access
- `ME_CONFIG_MONGODB_ADMINUSERNAME`: Admin username
- `ME_CONFIG_MONGODB_ADMINPASSWORD`: Admin password
- `ME_CONFIG_MONGODB_AUTH_USERNAME`: Authentication username
- `ME_CONFIG_MONGODB_AUTH_PASSWORD`: Authentication password
- `ME_CONFIG_BASICAUTH_USERNAME`: Basic auth username for the web interface
- `ME_CONFIG_BASICAUTH_PASSWORD`: Basic auth password for the web interface

## Access Information
- MongoDB: `localhost:27017`
- mongo-express web interface: `http://localhost:8081`
- Admin Username: as defined in your `.env` file
- Admin Password: as defined in your `.env` file

## Connection String Examples
### MongoDB URI Format
```
mongodb://username:password@localhost:27017/database?authSource=admin
```

### Node.js (with Mongoose)
```javascript
const mongoose = require('mongoose');
mongoose.connect('mongodb://username:password@localhost:27017/database?authSource=admin', {
  useNewUrlParser: true,
  useUnifiedTopology: true
});
```

### Python (with PyMongo)
```python
from pymongo import MongoClient
client = MongoClient('mongodb://username:password@localhost:27017/?authSource=admin')
db = client['database']
```

### Java (with MongoDB Java Driver)
```java
MongoClient mongoClient = MongoClients.create(
    "mongodb://username:password@localhost:27017/?authSource=admin"
);
MongoDatabase database = mongoClient.getDatabase("database");
```

### Go (with mgo)
```go
session, err := mgo.Dial("mongodb://username:password@localhost:27017/?authSource=admin")
if err != nil {
    panic(err)
}
defer session.Close()
```

## Notes
- The default image uses the latest version of MongoDB
- Data is persisted in a Docker volume named `mongodb`
- Access MongoDB directly using the configured credentials
- Manage MongoDB through the mongo-express web interface at http://localhost:8081
- The MongoDB container exposes port 27017 for external connections
