razor-client
============

A simple Dockerfile to provide `razor-client` in a Docker container.
This is intended to be used with `fadenb/razor-server`.

## Usage
Execute `docker run --rm -it --link razor-server razor-client`

The container defaults to `ENV RAZOR_API=http://razor-server:8080/api`.

