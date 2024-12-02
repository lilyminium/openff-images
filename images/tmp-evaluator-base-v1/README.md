# Creating a Docker image


Here is an example of creating an image and pushing it to GitHub.

```
IMAGE_NAME='tmp-evaluator-base-v0'
docker build --platform linux/amd64 --tag $IMAGE_NAME .
docker tag $IMAGE_NAME "ghcr.io/lilyminium/openff-images:${IMAGE_NAME}"
docker push "ghcr.io/lilyminium/openff-images:${IMAGE_NAME}"
```

The Dockerfile copies directly from the Dask docker image, which as of this time of writing is BSD-3 licensed.

