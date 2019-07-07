### Docker Machine

To Install Docker-Machine, 
1. create a dedicated EC2 machine as Docker-Machine and Install the docker-machine as follows

```sh
$ base=https://github.com/docker/machine/releases/download/v0.16.0 && curl -L $base/docker-machine-$(uname -s)-$(uname -m) >/tmp/docker-machine
$ sudo install /tmp/docker-machine /usr/local/bin/docker-machine
```
Then, check whether it is installed
```sh
/usr/local/bin/docker-machine ls
```
Now you need to configure Docker-Client (AWS) from Docker Machine, then follow the things

```sh
/usr/local/bin/docker-machine create --driver=amazonec2 --amazonec2-access-key DWCFKXT7CW7Q --amazonec2-secret-key S4XZExEWAruS+OlV9ZMzgOgGp --amazonec2-region us-east-2 dm1
```

If you want to install docker on standalone machine then provide the ip address and name
```sh
$ docker-machine create --driver none --url=tcp://50.134.234.20:2376 custombox
```

| TOPIC | LINK |
| ---- | -----|
| Docker Machine Installation| https://docs.docker.com/machine/install-machine/|
|Configuring the cloud providers |https://docs.docker.com/machine/get-started-cloud/ |
|Configuring the AWS EC2 Driver| https://docs.docker.com/machine/examples/aws/|
