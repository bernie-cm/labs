## Running multiple containers with Docker Compose
The idea is to create a single docker compose file that can be used to "orchestrate" different containers for an application. The efficiency is that you don't have to run separate, individual docker commands to start and stop containers.

# Define the services
- Each "service" in docker compose represents one building block, or container in your application
- In this example, we have a simple two-container database with mongodb and mongo-express
- This docker compose then has two services: mongodb for the mongo container, and mongo-express for the express container

# Set up the dependencies
- One important configuration is to set up `depends_on` properties correctly so the start order is correct
- For example, here we want to wait to start mongo-express **until after** the mongodb container is running

# No need to set up a network
- When two or more containers are run separately to deploy an application, a network has to be set up. For example, `mongo-network` to enable these two independent containers to communicate with each other
- When using docker compose, it will take care of creating a default network, in this case called `docker_default`

# Running and stopping the compose application
- The commands to start or stop the application are simple
```
$ docker compose up # or add the -d flag to push it to the background
$ docker compose down
```