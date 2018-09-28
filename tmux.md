## Usage

## Refreshing Config

From within a tmux session

``` bash
:source-file ~/.tmux.conf
```
or

``` bash
tmux source ~/.tmux.conf
```

## Modify windows

* Swap windows
  ```
  ctrl+b : swap-window -s 3 -t 1
  ```

* Move existing window to new position

  ```
  ctrl+b : move-window -t <POSITION>
  ```
