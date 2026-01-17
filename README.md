# zephyrrtos-docker
A docker image that can be used as a development environment with VS Code for developing projects that use Zephyr RTOS.

## Introduction
This docker image uses the [CI image provided by the Zephyr Project](https://github.com/zephyrproject-rtos/docker-image) as it's base. This insalls the dependencies to use Zephyr RTOS. It also installs the Zephyr Toolchain as well as the nRF Connect SDK toolchain.

There are 4 files in the repo, we are using **Dockerfile.dev** for developing Zephyr Applications, this also pulls in **Dockerfile.ci** as it's base which is used for Github workflows Continuous Integration on Github.

## New Package

Merging an open pull request against main branch will kick off a new package generation for the Docker Files that changed.  These new packages are automatically tagged with the amd64 tag and they will get pulled into the development environment automatically once they have finished building when you run **Ctrl + Shift + P >> Dev Containers: Rebuild Container** within Vscode
