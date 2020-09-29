# OpenJDK-8-JRE and Python3 base docker image #

**Author**: Teng Fu

**Contact**: teng.fu@teleware

## Aim ##

Due to the license change of Java, the openjdk-8-jdk/jre are removed from basic apt-get repo list, which causes following errors in JDK installation

```
E: could not locate openjdk-8-jdk
---
Errors were encountered while processing:
 openjdk-11-jre-headless:amd64
 openjdk-11-jre:amd64
 openjdk-11-jdk-headless:amd64
 default-jre
 default-jdk-headless
 openjdk-11-jdk:amd64
 default-jdk
E: Sub-process /usr/bin/dpkg returned an error code (1)

```

The solution here is use openjdk DockerHub as base image and further installed with Python3.

Python 3.7 slim: [https://github.com/docker-library/python/blob/35d8d9712c3ea4cbc4004a0e62ab61100b6fed99/3.7/buster/slim/Dockerfile](https://github.com/docker-library/python/blob/35d8d9712c3ea4cbc4004a0e62ab61100b6fed99/3.7/buster/slim/Dockerfile)

openJDK 8 slim: [https://github.com/docker-library/openjdk/blob/master/8/jre/slim-buster/Dockerfile](https://github.com/docker-library/openjdk/blob/master/8/jre/slim-buster/Dockerfile)

## Docker CMD ##

DockerHub repo: [here](https://hub.docker.com/repository/docker/tftwdockerhub/openjdk-8-jre_python3_debian_slim_base)

Pull:

```
sudo docker pull tftwdockerhub/openjdk-8-jre_python3_debian_slim_base:latest
```