# cpp_dockerfile

A Docker image to support [cpp_boilerplate_project](https://github.com/cpp-best-practices/cpp_boilerplate_project)
and [cpp_starter_project](https://github.com/cpp-best-practices/cpp_starter_project).

This container collects a large quantity of Linux C++ tools in one container, so you don't have to
install them all manually. 

A synopsis of the tools installed:

* Ubuntu 20.04
* gcc 11.1.0
* llvm/clang/clang-tidy/lldb/lld/clangd/libclang 13.0.1
* python3 3.8.10
* pip 22.0.4
* conan 1.47.0
* cmake/ccmake 3.23.0
* cppcheck 1.90
* doxygen 1.8.17
* include-what-you-use 0.17


# Usage

You must have Docker, or an equivalent substitute (podman, lima, etc) installed.
You do not need to check out this repository; you may pull prebuilt images directly
from Github Container Repository.

Run this in a terminal:

```bash
docker pull ghcr.io/ddalcino/cpp_starter:latest
docker run --entrypoint=/bin/bash -it cpp_starter:latest
```

You can build your own Dockerfiles that extend this Dockerfile:

```dockerfile
FROM ghcr.io/ddalcino/cpp_starter:0.1.0

# Install some packages here ...
```
