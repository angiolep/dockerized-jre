# open-jre
This Docker image provides extends [alpine](https://hub.docker.com/_/alpine/) and provides a minimal dockerized JRE - Java Runtime Environment:

* [OpenJRE](http://openjdk.java.net/) == 1.8.0_172
* [Linux Alpine](https://www.alpinelinux.org) == 3.8


## build

```bash
registry="registry.alpinedata.tech"
tag="dockerized/open-jre:8u171"
context="$(pwd)"

docker build \
  -t $registry/$tag \
  $context

docker tag \
  $registry/$tag \
  $tag  
```


## push

```bash
# You username at the registry
username="pangiolet"

docker login \
  --username $username \
  $registry

docker image push \
  $registry/$tag
```

## usage
This image is meant to be extended by others providing Java applications.
