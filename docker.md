### Set proxy in docker
```
sudo mkdir -p /etc/systemd/system/docker.service.d
sudo vi /etc/systemd/system/docker.service.d/proxy.conf

[Service]
Environment="HTTP_PROXY=http://myproxy.hostname:8080"
Environment="HTTPS_PROXY=https://myproxy.hostname:8080/"
Environment="NO_PROXY="localhost,127.0.0.1,::1"

sudo systemctl daemon-reload
sudo systemctl restart docker.service
```
### Get clean ubuntu 16 ###
```
docker pull ubuntu:16.04
docker run -it --name ub16 ubuntu:16.04 
```
### Run Docker without SUDO/root
```
sudo groupadd docker
sudo usermod -aG docker $USER
newgrp docker 
```
#### Test
```
docker run hello-world
```
### Input parameter to dockerfile ###
Dockerfile:
```
FROM ubuntu:16.04
ENV http_proxy $HTTP_PROXY
ENV https_proxy $HTTP_PROXY

```

docker build . -t docker_image_name \
--build-arg HTTP_PROXY=http://x.x.x.x:8888/ \
--build-arg HTTPS_PROXY=http://x.x.x.x:8888/

### Show CPU cores
```
taskset -c -p $$
pid 284307's current affinity list: 0-111
```

### Update run parameter
```
docker stop caffe
docker update -c 512 caffe
docker start caffe
```

### List all containers (only IDs)
`docker ps -aq`

### Stop all running containers
`docker stop $(docker ps -aq)`

### Remove all containers
`docker rm $(docker ps -aq)`

### Remove all images
`docker rmi $(docker images -q)`

### Save image to tar file
```
docker save demo > latest.tar
```
### Load image from tar file
docker load --input latest.tar

### Export container to tar file
```
docker export demo > latest.tar
```
### Import container from tar file
```
docker import latest.tar container_name
```
### Commit container to image

```
sudo docker commit deddd39fa163 ubuntu-nmap
```
