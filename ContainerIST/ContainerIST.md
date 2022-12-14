# 💤 Overview:

- List all available container on system:

```shell
docker ps -a
```

- List all running container:

```shell
docker ps
```

- Restart a Docker container:

```shell
docker start containerName
docker start containerId
```

```shell
docker start ubuntu-container
docker start fb2d7e3e2bb4
```

- Attach to Docker container:

```shell
docker attach containerName
docker attach containerId
```

```shell
docker attach ubuntu-container
docker attach fb2d7e3e2bb4
```

- Stop a Docker container

```shell
docker stop containerName
docker stop containerId
```

```shell
docker stop ubuntu-container
docker stop fb2d7e3e2bb4
```

- Delete a Docker container:

```shell
docker rm containerName
docker rm containerId
```

```shell
docker rm -f Ubuntu
docker rm -f 8d489149aadd
```

- Execute a command via a Docker container:

```shell
docker exec containerName command
docker exec containerId command
```

```shell
docker exec Ubuntu cat /etc/*release
docker exec 8d489149aadd cat /etc/*release
```

- Save a Docker container:

```shell
docker commit containerName image[:tag]
docker commit containerId image[:tag]
```

```shell
docker commit containerName image[:tag]
docker commit containerId image[:tag]
```
