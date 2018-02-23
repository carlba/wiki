# Tweaks

## Make updatedb command available in macOS

``` bash
sudo ln -s /usr/libexec/locate.updatedb /usr/local/bin/updatedb
```
### Autocomplete ssh hostnames

``` bash
brew install bash-completion
brew tap homebrew/completions
```

Then add the following to your ~/.bash_profile:
``` bash
if [ -f $(brew --prefix)/etc/bash_completion ]; then
. $(brew --prefix)/etc/bash_completion
fi
```

## Make the dock faster

[Stack Exchange](https://apple.stackexchange.com/questions/33600/how-can-i-make-auto-hide-show-for-the-dock-faster)

To make the Dock instantly leap back into view when it’s needed, rather than slide,
open a Terminal window and type the following:

```
defaults write com.apple.dock autohide-time-modifier -int 0;killall Dock
```
I find this useful, but if you’d like the animation for the dock to reappear to last for a
split-second, try the following:

```
defaults write com.apple.dock autohide-time-modifier -float 0.15;killall Dock
```

To revert back to the default sliding effect, open a Terminal window and type the following:

```
defaults delete com.apple.dock autohide-time-modifier;killall Dock
```

## Dramatically Speed Up Window Resizing Animation Speed in Mac OS X

```
defaults write -g NSWindowResizeTime -float 0.003
```

### Figure out ip address of interface

``` bash
ifconfig |grep inet
```

## Clear local Time Machine snapshots

``` bash
tmutil  listlocalsnapshotdates / |grep 20|while read f; do tmutil deletelocalsnapshots $f; done
```

Taken from
https://forums.macrumors.com/threads/how-to-delete-time-machine-local-backups-on-high-sierra.2073998/

## nginx

http://learnaholic.me/2012/10/10/installing-nginx-in-mac-os-x-mountain-lion/

* homebrew default nginx config

    ```
    /usr/local/etc/nginx/nginx.conf
    ```


* homebrew default nginx log

    ```
    /usr/local/var/log/nginx/access.log
    ```

## KeePass

``` bash
brew cask install macpass
```

## Sublime

* User packages
    ``` bash
    $HOME/Library/Application\ Support/Sublime\ Text\ 3/Packages/User
    ```
* Installed Packages
    ``` bash
    $HOME/Library/Application\ Support/Sublime\ Text\ 3/Installed\ Packages
    ```

## Transmission Remote GUI
```bash
brew cask install transmission-remote-gui
```

## Android ADB
```bash
brew cask install android-platform-tools
```

## Journey
```bash
brew cask install journey
```


## Alfred

### Make pirated Alfred stop asking for contact permission
```bash
sudo codesign --force --deep --sign - /Applications/Alfred\ 3.app/Contents/Frameworks/Alfred\ Framework.framework/
```

## Iterm2

### Change Tab Size

``` bash
defaults write com.googlecode.iterm2 OptimumTabWidth -int 500
```

## dash
``` bash
brew cask install dash
```

## Add user to admin group
``` bash
sudo dseditgroup -o edit -a $username_to_add -t user admin
sudo dseditgroup -o edit -a $username_to_add -t user wheel
```

http://macappstore.org/pigz/

