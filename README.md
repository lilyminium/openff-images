# openff-images
Docker images for OpenFF projects



## Set up instructions

Below are instructions for pushing your own images. Step 1 is to have Docker installed and running.

### Log in to ghcr.io

Create a personal access token with package permissions and set it as `GH_TOKEN=...`

Log in:

```
echo $GH_TOKEN | docker login ghcr.io -u $GITHUB_USERNAME --password-stdin
```

### Make packages public

Navigate to the url: https://github.com/users/lilyminium/packages/container/package/openff-images

Click "Package settings" on the right-hand sidebar. Scroll down to the Danger zone and make it public.