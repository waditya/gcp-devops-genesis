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

```console
admin@docker-host:~/gcp-devops-project$ docker images
REPOSITORY            TAG       IMAGE ID       CREATED          SIZE
python-docker-image   latest    47ea3d67130c   13 seconds ago   129MB
<none>                <none>    54d90786d46b   2 minutes ago    129MB
<none>                <none>    4eb99edba74c   6 minutes ago    129MB
```

3. Command to run a docker image

```shell
docker run -p 5000:5000 python-docker-image
```

```console
admin@docker-host:~/gcp-devops-project$ docker run -p 5000:5000 python-docker-image
 * Debug mode: off
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on all addresses (0.0.0.0)
 * Running on http://127.0.0.1:5000
 * Running on http://172.12.0.2:5000
Press CTRL+C to quit
172.12.0.1 - - [25/Sep/2024 03:52:11] "GET / HTTP/1.1" 200 -
172.12.0.1 - - [25/Sep/2024 03:52:28] "GET / HTTP/1.1" 200 -
172.12.0.1 - - [25/Sep/2024 03:53:29] "GET / HTTP/1.1" 200 -
172.12.0.1 - - [25/Sep/2024 04:06:12] "GET / HTTP/1.1" 200 -
172.12.0.1 - - [25/Sep/2024 04:06:14] "GET / HTTP/1.1" 200 -
172.12.0.1 - - [25/Sep/2024 04:06:44] "GET / HTTP/1.1" 200 -
172.12.0.1 - - [25/Sep/2024 04:06:47] "GET / HTTP/1.1" 200 -
172.12.0.1 - - [25/Sep/2024 04:06:48] "GET / HTTP/1.1" 200 -
172.12.0.1 - - [25/Sep/2024 04:06:49] "GET / HTTP/1.1" 200 -
172.12.0.1 - - [25/Sep/2024 04:06:50] "GET / HTTP/1.1" 200 -
172.12.0.1 - - [25/Sep/2024 04:06:50] "GET / HTTP/1.1" 200 -
172.12.0.1 - - [25/Sep/2024 04:06:51] "GET / HTTP/1.1" 200 -
172.12.0.1 - - [25/Sep/2024 04:06:52] "GET / HTTP/1.1" 200 -
```

4. Testing the Application


```console
admin@docker-host:~$ curl http://localhost:5000 && echo ""
Hello, Simple Flask Application
admin@docker-host:~$ curl http://localhost:5000 && echo ""
Hello, Simple Flask Application
admin@docker-host:~$ 
admin@docker-host:~$ curl http://localhost:5000 && echo ""
Hello, Simple Flask Application
```