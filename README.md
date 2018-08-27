razor-client
============

A simple Dockerfile to provide `razor-client` in a Docker container.
This is intended to be used with `fadenb/razor-server`.

## Usage
The container defaults to `ENV RAZOR_API=http://razor-server:8080/api`.

Execute `docker run --rm -it --link razor-server razor-client` to get list of commands from the `razor-server`.
Execute `docker run --rm -it --link razor-server razor-client PARAMETER` to execute `razor-client` with the specified command line parameters.

## Examples
### List tasks
```
$ docker run --rm -it --link razor-server fadenb/razor-client tasks debian                                                                                                                        ~/code/bcc/razor-client
From http://razor-server:8080/api/collections/tasks/debian:

         name: debian
  description: Debian Generic Installer
           os:
                 version: wheezy
     boot_seq:
                       1: boot_install
                 default: boot_local

Query additional details via: `razor tasks debian [boot_seq, os]`

```
