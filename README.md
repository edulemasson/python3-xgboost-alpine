# XGBoost + Docker + Alpine

This is a base image configured to serve as base image to work with Python3 XGBOOST pre-built with all dependencies and compiled in Alpine Linux Kernel.
.


# How to use in your project

Create a Dockerfile that extends  [eduardolemasson](https://hub.docker.com/u/eduardolemasson/)/[xgboost-alpine](https://hub.docker.com/r/eduardolemasson/xgboost-alpine/) that mounts your source-files volume and set the entrypoint to your main application. You can find a complete example in Example folder.
