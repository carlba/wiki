# Installation

Run this in an elevated command prompt

```powershell
@powershell -NoProfile -ExecutionPolicy Bypass -Command "iex ((new-object net.webclient).DownloadString('https://chocolatey.org/install.ps1'))" && SET PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin
```

## Installed packages
### General

Use the ``--allow-empty-checksums-secure`` to prevent validating checksums

```cmd
choco install -y ccleaner chocolateygui dropbox SublimeText3 SublimeText3.PackageControl sublimetext3-contextmenu spotify javaruntime google-chrome-x64 skype python2 cygwin virtualbox virtualbox.extensionpack steam irfanview adobereader revo.uninstaller defraggler winrar wincdemu
```

### Work
```cmd
choco install vmwarevsphereclient
```

# Usage

## Install package

```cmd
choco install <packagename>
cinst <packagename>
```
* -y force install

## Uninstall package
```cmd
choco uninstall <packagename>
```
* -y force uninstall

## Upgrade all packages

```cmd
cup all
```

# Links
https://chocolatey.org/
