### get clean ubuntu 16 ###
```
docker pull ubuntu:16.04
docker run -it --name ub16 ubuntu:16.04 
```

### input parameter to dockerfile ###
Dockerfile:
```
FROM ubuntu:16.04
ENV http_proxy $HTTP_PROXY
ENV https_proxy $HTTP_PROXY
...
```

docker build . -t docker_image_name \
--build-arg HTTP_PROXY=http://x.x.x.x:8888/ \
--build-arg HTTPS_PROXY=http://x.x.x.x:8888/

### show CPU cores
```
taskset -c -p $$
pid 284307's current affinity list: 0-111
```

### update run parameter
```
docker stop caffe
docker update -c 512 caffe
docker start caffe
```

### List all containers (only IDs)
docker ps -aq

### Stop all running containers
docker stop $(docker ps -aq)

### Remove all containers
docker rm $(docker ps -aq)

### Remove all images
docker rmi $(docker images -q)
