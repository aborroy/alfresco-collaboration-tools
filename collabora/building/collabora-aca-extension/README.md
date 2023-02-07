This folder contains internal configuration to build the `collabora-aca-extension` Angular component. 

It shouldn't be required to be executed, since `collabora-aca-extension-0.6.0-dist.tgz` is included in [../aca-collabora](../aca-collabora) folder.

## Build Docker Image

```
$ docker build . -t collabora-aca-extension
```

## Get Package

```
$ docker run -v $(pwd):/target collabora-aca-extension

$ ls c*
collabora-aca-extension-0.6.0-dist.tgz
```

## Copy package

```
$ cp collabora-aca-extension-0.6.0-dist.tgz ../aca-collabora/extensions
```
