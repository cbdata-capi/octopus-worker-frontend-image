# About `octopus-worker-frontend-image`

This contains source for Docker image with tools to deploy our frontends from Octopus deploy worker node. 
It extends `octopusdeploy/worker-tools` with `npm` and other tools needed.

## Deployment

GitHub action on change in `[main]` will trigger build of `*:main` image.
To publish a version, push tag in format `v*.*.*`.

## Local Testing

To build image, create and run container and to attach the container:
```
docker build . --tag octopus-worker-frontend-image:build
docker run -it octopus-worker-frontend-image:build
```