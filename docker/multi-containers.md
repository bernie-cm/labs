## How to run multiple containers for an application

## Running mongo as database
- Create a network to be shared between mongo-express and mongodb
```
docker network create mongo-network
```
- Using the mongo image, create a container with the required environment variables
- Check container is running as expected

### Troubleshooting
- Initial configuration didn't work, so had to include two additional environment variables when running the mongo-express container `BASIC_AUTH_USERNAME` and `BASIC_AUTH_PASSWORD`
```
docker run -d -p 8081:8081 -e ME_CONFIG_MONGODB_ADMINUSERNAME=admin -e ME_CONFIG_MONGODB_ADMINPASSWORD=password -e ME_CONFIG_BASICAUTH_USERNAME=admin -e ME_CONFIG_BASICAUTH_PASSWORD=password --net mongo-network --name mongo-express -e ME_CONFIG_MONGODB_SERVER=mongodb -e ME_CONFIG_MONGODB_URL=mongodb://mongodb:27017 mongo-express
```