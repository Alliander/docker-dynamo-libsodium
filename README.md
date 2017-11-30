## Docker image for standard image with Libsodium

Libsodium is an encryption / decryption library that is used in USEF to encrypt and decrypt messages.

Create / update the image can be done by:
```console
$ docker build --no-cache -t usefdynamo/libsodium:0.3 .
```

To have this image available in the K8S environment it needs to be pushed to the usefdynamo repository:
```console
$ docker push usefdynamo/libsodium:0.3
```

* Check the version number before you carry out these commands! The intention is that these repos will be automatically built by Docker Hub or Quay.io. At the moment it is still not ready and needs to be pushed manually to the repo. *
