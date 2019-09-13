# Samsung

## Debloat

### List all services

```bash
adb shell pm list packages
```

### List disabled services

```bash
adb shell pm list packages -d
```

### Disable service

```bash
adb shell pm disable-user --user 0 <package_name>
```

### Disabled on Samsung Galaxy S10 Plus

com.samsung.android.game.gamehome
com.dsi.ant.service.socket
com.dsi.ant.sample.acquirechannels
com.samsung.android.aircommandmanager
com.samsung.android.messaging
com.dsi.ant.plugins.antplus
com.dsi.ant.server
com.samsung.android.samsungpass
com.samsung.android.scloud
com.samsung.android.providers.contacts
com.samsung.android.bixby.agent.dummy

pm enable-user --user 0 com.samsung.android.providers.contacts
