# 💤 Overview:

- List all available images on system:

```shell
docker images
```

- Search Docker image

```shell
docker search imageName

```

```shell
docker search ubuntu
```

- Pull a Docker image:

```shell
docker pull imageName[:tag]

```

```shell
docker pull ubuntu:20.04

```

- Remove a Docker image:

```shell
docker image rm imageName[:tag]
docker image rm imageId
```

```shell
docker image rm ubuntu:20.04
docker image rm 6b7dfa7e8fdb
```

- Run a Docker image:

```shell
docker run [option] imageName [command] [args]
docker run [option] imageId [command] [args]
```

```shell
docker run -it --name "Ubuntu" -h "Ubuntu" ubuntu:20.04
docker run -it --name "Ubuntu" -h "Ubuntu" 6b7dfa7e8fdb
```

- Save a Docker image to tar:

```shell
docker save --output filePath.tar imageName
docker save --output filePath.tar imageId
```

```shell
docker save --output ubuntu-nano.tar Ubuntu
docker save --output ubuntu-nano.tar 6b7dfa7e8fdb
```

- Load a Docker image from tar:

```shell
docker load --i filePath.tar
```

```shell
docker load --i ubuntu-nano.tar
```

- Change a Docker image name:

```shell
docker tag imageId imageName[:tag]
```

```shell
docker tag 6b7dfa7e8fdb ubuntu-nano
```
