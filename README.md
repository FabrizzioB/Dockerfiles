# Dockerfiles

This repository is to aid the learning of Docker containers.
Provides commands, tips and hints, Dockerfiles and docker-compose files.

Enjoy!

***

## Commands

- To check for all containers
```bash
docker ps
```

- To check for all containers alive
```bash
docker ps -a
```

- To remove a docker image(s)
```bash
docker rmi <image_id1> <image_id2> 
```

- To build an image
```bash
docker build -t <desired_image_name> . 
```

- Check the images created
```bash
docker images
```

- Execute the container you just created the image of
```bash
docker run -d --name <image> -e <environment-variables=...> -p <port host:port container> <container-name>
```

- To see the logs of a container
```bash
docker logs <image_id>
```



### Run the containers
---

Run container postgresql:
```bash
docker run -d --name postgres_container -e POSTGRES_PASSWORD=mypassword -p 5433:5432 postgresql_container
```

