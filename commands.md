# Commands to run the Docker Container 

1. Command to create image locally 

```shell
docker build --tag python-docker-image .
```

```console
admin@docker-host:~/gcp-devops-project$ docker build --tag python-docker-image .
[+] Building 30.9s (10/10) FINISHED                                                                                  docker:default
 => [internal] load .dockerignore                                                                                              0.0s
 => => transferring context: 2B                                                                                                0.0s
 => [internal] load build definition from Dockerfile                                                                           0.0s
 => => transferring dockerfile: 227B                                                                                           0.0s
 => [internal] load metadata for docker.io/library/python:3.8-slim-buster                                                     30.2s
 => [internal] load build context                                                                                              0.0s
 => => transferring context: 288B                                                                                              0.0s
 => [1/5] FROM docker.io/library/python:3.8-slim-buster@sha256:8799b0564103a9f36cfb8a8e1c562e11a9a6f2e3bb214e2adc23982b36a045  0.0s
 => CACHED [2/5] WORKDIR /app                                                                                                  0.0s
 => CACHED [3/5] COPY requirements.txt requirements.txt                                                                        0.0s
 => CACHED [4/5] RUN pip3 install -r requirements.txt                                                                          0.0s
 => [5/5] COPY . .                                                                                                             0.0s
 => exporting to image                                                                                                         0.7s
 => => exporting layers                                                                                                        0.7s
 => => writing image sha256:47ea3d67130cc34f61039f493bfcc4c3b54c1b72477331b5c7b917d61c936e88                                   0.0s
 => => naming to docker.io/library/python-docker-image                                                                         0.0s
```

2. Command to list the image

```shell
docker images
```

3. Command to run a docker image

```shell
docker run -p 5000:5000 python-docker-image
```