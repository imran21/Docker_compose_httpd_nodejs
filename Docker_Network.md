### Docker Networking


Create a network in Docker


```sh

$ docker network create --driver bridge  nw1 --subnet 192.168.0.1/29 --gateway 192.168.0.1

```

Then Create a container on that network

```sh
$ docker run -ti --name mn1 --net=nw1 --ip 192.168.0.2 centos:latest /bin/bash
```
If IP address got over in the pool then you will get the following ERROR message

```sh
> docker: Error response from daemon: No available addresses on this pool.

```
