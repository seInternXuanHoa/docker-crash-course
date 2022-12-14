# 💤 Network:

- List all Docker network:

```shell
docker network ls
```

- Get Docker network info:

```shell
docker network inspect networkName
```

```shell
docker network inspect bridge
```

- Set Port for Docker container:

```shell
docker run [option] imageName [command] [args]
docker run [option] imageId [command] [args]
```

```shell
docker run -it --name "BusyBox" -h "BusyBox" -v prev:/home/prev -p 81:80 busybox
```

- Create a Docker network:

```shell
docker network create --driver driverType networkName
```

```shell
docker network create --driver bridge prev
```

- Delete a Docker network:

```shell
docker network rm networkName
```

```shell
docker network rm prev
```

- Set network for docker containter:

```shell
docker run [option] imageName [command] [args]
docker run [option] imageId [command] [args]

```

```shell
docker run -it --name "BusyBox" -h "BusyBox" -v prev:/home/prev -p 81:80 --network prev busybox

```

- Add Docker container to a network:

```shell
docker network connect networkName containerName
```

```shell
docker network connect prev BusyBox
```
