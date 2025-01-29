# Creating a Docker image


Here is an example of creating an image and pushing it to GitHub. 

```
IMAGE_NAME='protein-benchmark-nagl-base-v0'
docker build --platform linux/amd64 --tag $IMAGE_NAME .
docker tag $IMAGE_NAME "ghcr.io/lilyminium/openff-images:${IMAGE_NAME}"
docker push "ghcr.io/lilyminium/openff-images:${IMAGE_NAME}"
```
