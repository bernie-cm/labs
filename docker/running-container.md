## How to run a Redis container

### Pulling and running a Redis image
- Use the command `docker pull redis:latest`
- Then run `docker run -d --name my-redis -p 6379:6379 redis:latest`. This will bind the container's Redis port to my host machine.

### Starting and stoppign the container
- Once the container is running, you can simply stop it by running `docker stop [container-name]`
- For example, you can get a list of running containers by using `docker ps`
- To stop the container run `docker stop 2ac` (using the first 3 characters is enough to identify the container, but you can also use the container's name `my-redis`).
- To start the container again use `docker start 2ac`.

### Inspecting logs and getting a shell
- To inspect logs use `docker logs 2ac | my-redis`.
- Finally, if you need to get a shell use `docker exec -it my-redis /bin/sh|/bin/bash`