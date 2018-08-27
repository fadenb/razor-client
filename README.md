razor-client
============

A simple Dockerfile to provide `razor-client` in a Docker container.
This is intended to be used with `fadenb/razor-server`.

## Usage
The container defaults to `ENV RAZOR_API=http://razor-server:8080/api`.

Execute `docker run --rm -it --link razor-server razor-client` to get list of commands from the `razor-server`.
Execute `docker run --rm -it --link razor-server razor-client PARAMETER` to execute `razor-client` with the specified command line parameters.

