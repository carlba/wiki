Installation
============

<https://docs.docker.com/engine/installation>

1.  Docker The easiest way to install Docker on major linux
    distributions is

    ``` sourceCode
    wget -qO- https://get.docker.com/ | sudo sh
    ```

2.  docker-compose

    Compose is a tool for defining and running multi-container Docker
    applications. With Compose, you use a Compose file to configure your
    application’s services. Then, using a single command, you create and
    start all the services from your configuration.

    ``` sourceCode
    sudo pip install docker-compose
    ```

3.  shipyard

    [Shipyard] is a UI that simplifies the sometimes tedious task of
    managing your images and instances.

    ``` sourceCode
    curl -s https://shipyard-project.com/deploy | sudo bash -s
    ```

Usage
=====

This information is provided in a verbose version at [Get started with
Docker guide]. I recommend reading through that and the rest of the
Docker documentation for a more thorough understanding of the subject.

Basics
------

1.  `docker ps` - List the state of your Docker containers

Building Docker images locally
------------------------------

``` sourceCode
sudo docker build -t docker.smithmicro.net/passport:latest .
```

<table style="width:81%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 65%" />
</colgroup>
<thead>
<tr class="header">
<th>Argument</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-t</td>
<td>Name the image</td>
</tr>
</tbody>
</table>

Pushing Docker image to registry
--------------------------------

``` sourceCode
sudo docker push docker.smithmicro.net/passport:latest
```

Running Docker containers
-------------------------

``` sourceCode
sudo docker run --name passport -p 8002:8002 docker.smithmicro.net/passport:latest
```

### Mounting volumes

``` sourceCode
sudo docker run --name passport --volume $PWD/logs:/var/log/smsi/passport -p 8002:8002 docker.smithmicro.net/passport:latest
```

### Access container with bash

``` sourceCode
sudo docker exec -i -t {container_name} /bin/bash
```

<table style="width:90%;">
<colgroup>
<col style="width: 18%" />
<col style="width: 71%" />
</colgroup>
<thead>
<tr class="header">
<th>Argument</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>--name</td>
<td>Name the instance</td>
</tr>
<tr class="even">
<td>--volume/-v</td>
<td>Mount a container volume to the host. Use $PWD to mount to the current folder.</td>
</tr>
</tbody>
</table>

<https://docs.docker.com/engine/reference/run/>

Monitoring
==========

[Glances] is a good tool for monitorin

  [Shipyard]: https://github.com/shipyard/shipyard
  [Get started with Docker guide]: https://docs.docker.com/engine/getstarted/
  [Glances]: 
