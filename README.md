# Simple demontration on the use of ArgoCD

This is the application repository where we emulate the typical Developer experience of creating an application and deploying it to an container image repository. The example we will use here is Docker Hub, however, the same can be achieved on any Image repository like Amazon's ECR.

## Getting started

### Create Container Image

**Optional and for demonstration purposes only.**

We will be using Docker Hub as an Image repository.

Please sign in
```sh
docker login
```
Or you can specify your account as follows. Please use your own account. Mine is nabeelhamad893
```sh
docker login --username nabeelhamad893
```

Push image to your Image repository account

In this example, we will push a standard nginx image, with our own tag, to our account. The tag will demonstrate a typical Developer deployment of an image deployment

```sh
docker pull nginx:1.29.0
docker tag nginx:1.29.0 nabeelhamad893/nginx:v0.1.0
```

Now lets push the newly created image with our tag
```sh
docker push nabeelhamad893/nginx:v0.1.0
```

### Running

