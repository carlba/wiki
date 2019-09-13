# Usage

## Kill And Remove Container

``` bash
docker rm -f CONTAINER_ID
```

## Remove all unused local volumes

[volume prune](https://docs.docker.com/engine/reference/commandline/volume_prune)

## MacOS debacle

```bash
rm -rf ~/Library/Containers/com.docker.docker/Data/vms/0/data/*
```

~/Library/Containers/com.docker.docker/Data/vms/0/data