# 💤 Volumes:

- Share directory from host and guest container:

```shell
docker run [option] imageName [command] [args]
docker run [option] imageId [command] [args]
```

```shell
docker run -it --name "Ubuntu" -h "Ubuntu" -v /volumes:/volume ubuntu:20.04
docker run -it --name "Ubuntu" -h "Ubuntu" -v /volumes:/volume 6b7dfa7e8fdb
```

- Quick create a container share same directory with difference container:

```shell
docker run [option] imageName [command] [args]
docker run [option] imageId [command] [args]
```

```shell
docker run -it --name "Ubuntu" -h "Ubuntu" --volumes-from "CentOS" ubuntu:20.04
docker run -it --name "Ubuntu" -h "Ubuntu" --volumes-from "CentOS" 6b7dfa7e8fdb
```

- List all Docker volume:

```shell
docker volume ls
```

- Create a Docker volume:

```shell
docker volume create volumeName [command]
```

```shell
docker volume create prev
docker volume create --opt device=/home/ist/prev --opt type=none --opt o=bind prev
```

- Get volume info:

```shell
docker volume inspect volumeName
```

```shell
docker volume inspect prev
```

- Remove a Docker Volume:

```shell
docker volume rm volumeName
```

```shell
docker volume rm prev
```

- Share volume from host and guest container:

```shell
docker run [option] imageName [command] [args]
docker run [option] imageId [command] [args]
```

```shell
docker run -it --name "Ubuntu" -h "Ubuntu" --mount source=prev,target=/home/prev ubuntu
docker run -it --name "Ubuntu" -h "Ubuntu" -v prev:/home/prev ubuntu
```
