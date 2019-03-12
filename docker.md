### get clean ubuntu 16 ###
```
docker pull ubuntu:16.04
docker run -it --name ub16 ubuntu:16.04 
```

### input parameter to dockerfile ###
Dockerfile:

FROM ubuntu:16.04
ENV http_proxy $HTTP_PROXY
ENV https_proxy $HTTP_PROXY
...


docker build . -t docker_image_name \
--build-arg HTTP_PROXY=http://x.x.x.x:8888/ \
--build-arg HTTPS_PROXY=http://x.x.x.x:8888/
