# Servern

## Usage

[Snapraid tutorial](http://zackreed.me/setting-up-snapraid-on-ubuntu/)

[Smartmon tutorial](http://zackreed.me/how-do-i-know-if-my-hard-drive-is-failing/)

## Docker containers

### Upgrade containers
```bash
cd /home/cada/docker/media-server
sudo docker-compose kill
sudo docker-compose pull
sudo docker-compose up -d
```

### snapraid

[Setting Up SnapRAID on Ubuntu](https://zackreed.me/setting-up-snapraid-on-ubuntu/)
[ArchLinux Wiki - SnapRAID](https://wiki.archlinux.org/index.php/SnapRAID)

#### Execute the snapraid sync script

```bash
sudo docker exec -it mediaserver_snapraid_1 /usr/bin/python2.7 \
    /app/snapraid-runner/snapraid-runner.py -c /config/snapraid-runner.conf
```

#### Execute a snapraid sync

```bash
sudo docker exec -it mediaserver_snapraid_1 snapraid sync
```

## FlexGet

### Execute Flexget with ``--discover-now``

[FlexGet Cli Reference](https://flexget.com/CLI)

```bash
sudo docker exec -it mediaserver_flexget_1 flexget -c /config/config.yml execute --discover-now --now
```

### Reset The Database

```bash
sudo docker exec -it mediaserver_flexget_1 flexget -c /config/config.yml database reset --sure
```

### Auth with trakt.tv

```bash
sudo docker exec -it mediaserver_flexget_1 flexget -c /config/config.yml trakt auth carlba
```

### Sync with Trakt.tv Collection

```bash
sudo docker exec -it mediaserver_flexget_1 flexget -c /config/config.yml execute --discover-now --tasks sync_collected_trakt
``
