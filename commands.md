# Commands to run the Docker Container 

1. Command to create image locally 

```shell
docker build --tag python-docker-image .
```

2. Command to list the image

```shell
docker images
```

3. Command to run a docker image

```shell
docker run -p 5000:5000 python-docker-image
```