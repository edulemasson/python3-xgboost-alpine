# XGBoost + Docker + Alpine

This is a base image configured to serve as base image to work with Python3 XGBOOST pre-built with all dependencies and compiled in Alpine Linux Kernel.
.


# How to use in your project

Create a Dockerfile that extends  [eduardolemasson](https://hub.docker.com/u/eduardolemasson/)/[xgboost-alpine](https://hub.docker.com/r/eduardolemasson/xgboost-alpine/) that mounts your source-files volume and set the entrypoint to your main application. You can find a complete example in Example folder.

## Example project
There is a Makefile in the sample folder that make it easy to work. You will just need to run two commands to deploy your project in Docker.
 1. Clone this repository and access the  **example**  folder in terminal.
 2. Execute the Build command to create your own docker image: sudo make build.
 3. Run your container: sudo make run

## Environment to deploy and develop
You can even use the docker environment to develop your project. Check it out the entire list of pre-defined commands in Makefile.
