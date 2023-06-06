# Docekr Commands

## Save , Load | Copy docker images to other host

Save the Docker image as a tar file:

```sh
docker save -o <path for generated tar file> <image name>
```

Load the image into Docker:

```sh
docker load -i <path to image tar file>
```
