
# Usage

## Autostart
https://github.com/nicolargo/glances/wiki/Start-Glances-through-Systemd

## Installation
``` bash
curl -L http://bit.ly/glances | /bin/bash
```

## Issues

### Sensors not showing

Install the latest version of psutil python library

``` bash
sudo pip install -U git+git://github.com/giampaolo/psutil.git
```

### Get lm-sensors working on servern

https://www.spinics.net/lists/lm-sensors/msg27465.html
