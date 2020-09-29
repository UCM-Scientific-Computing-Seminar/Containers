# Containers

This repo contains the config files, commands, and websites discussed in the talk "Containers for Scientific Computing and Data Science"

## Websites

- [Docker](https://www.docker.com/)
- [DockerHub](https://hub.docker.com/)
- [Podman](https://podman.io/)

### DockerHub Images

- [Fedora Official](https://hub.docker.com/_/fedora)
- [Ubuntu Official](https://hub.docker.com/_/fedora)
- [Clear Linux](https://hub.docker.com/_/clearlinux)
- [Julia Official](https://hub.docker.com/_/julia)
- [Tensor Flow](https://hub.docker.com/r/tensorflow/tensorflow/)
- [MPI](https://hub.docker.com/r/dispel4py/docker.openmpi/)

## Commands

```console
$ docker pull fedora:latest                                 # pulls fedora latest image
$ docker run -ti fedora:latest bash                         # run an interactive bash shell in fedora
$ docker run -ti ubuntu:latest bash                         # run an interactive bash shell in ubuntu
$ docker run -v "$(pwd)":/files -ti fedora:latest bash      # bash with access files in local directory
$ docker run -v "$(pwd)":/files -ti fedora:latest python3 /files/hello-world.py # non iteractive python script run
$ docker build -t myfedora:pip .                            # build custom fedora image
$ docker run -ti myfedora:pip bash                          # run bash in custom image
$ docker-compose run bash                                   # start bash "app" using compose
```