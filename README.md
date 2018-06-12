# About this repo

This is the Git repo forked from the official Docker images for [grpc][].

# Tags

- `groovex/grpc:cxx` (`cxx-1.12`): Container to build cxx with gRPC 1.12.x
- `groovex/grpc:python` (`python-1.12`): Container to run python 2.7 with gRPC 1.12.x
- `groovex/grpc:python-onbuild` (`python-1.12-onbuild`): Container to run python 2.7 with gRPC 1.12.x and custom requirements.txt
- `groovex/grpc:python3` (`python3-1.12`): Container to run python 3.6 with gRPC 1.12.x
- `groovex/grpc:python3-onbuild` (`python3-1.12-onbuild`): Container to run python3.6 with gRPC 1.12.x and custom requirements.txt


# What is gRPC ?

A high performance, open source, general RPC framework that puts mobile and
HTTP/2 first, available in many programming languages.  For full details, see
the official [gRPC documentation][].


# Organization

The repo is set up to mirror the structure of [docker-library][] repos.

- For each grpc release, there is a folder named after the release version.
- Within each release folder, there is a folder containing Dockerfiles for each of the supported grpc programming languages.
- Within each language folder, there is a main Dockerfile derived from the latest stable debian release and version of the programming language.
  - Optionally, there may be sub-folders containing other docker images, e.g, 'slim' versions or versions built at other versions of debian or the programming language

The folder structure matches that used by [official docker images][]. This
anticipates the future publishing gRPC as an official docker image once it
reaches it GA milestone.


[docker-library]:https://github.com/docker-library
[grpc]:http:/grpc.io
[official docker images]:https://github.com/docker-library/official-images
[grpc documentation]:http://www.grpc.io/docs/
