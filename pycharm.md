# Installation

# Usage

## Log

* MacOS

  ```bash
    tail -f /Users/cada/Library/Logs/PyCharm2018.3/idea.log
  ```

## Tweaks

I noticed weird terminal behavior and was able to fix that by setting

`-Dconsole.encoding=UTF-8` in `On the Help menu, click Edit Custom VM Options.`
(Configuring Output Encoding)[https://www.jetbrains.com/help/pycharm/configuring-output-encoding.html]



## Keyboard shortcuts

| Key combination         | Meaning                              |
|:------------------------|:-------------------------------------|
| ALT + 1                 | Goto Project overview                |
| ALT + 6                 | TODO                                 |
| ALT + 7                 | Structure overview                   |
| ALT + DOWN              | Show scopes                          |
| CTRL + mouse over       | Brief info                           |
| SHIFT + F1              | External Doc                         |
| CTRL + B                | Goto definition                      |
| CTRL + Numpad /         | Comment/Uncomment with line comment  |
| CTRL + SHIFT + Numpad / | Comment/Uncomment with block comment |
| CTRL + Shift + J        | Smart line join                      |
| CTRL + Enter            | Smart line split                     |
| ALT + Enter             | Quick fix issue under marker         |
| Shift + Command + 8     | Column Selection Mode                |
| CMD + K                 | Commit to VCS.                       |

## Fix Skiptest error

_jb_runner_tools.py

```python
class NewTeamcityServiceMessages(_old_service_messages):
    _latest_subtest_result = None

    def message(self, messageName, **properties):
        if messageName in set(["enteredTheMatrix", "testCount", "testIgnored"]):
```

## Themes

[Zenburn](https://github.com/darvin/JetBrains-ZenBurn)

### Ruby Syntax Highlighting in PyCharm
1. Enable `TextMate bundles support` plugin
2. ```bash
   git clone https://github.com/textmate/ruby.tmbundle ~/development
   ```
3. Goto `Editor > TextMate Bundles` and add the bundle

# Configuration

## Hide the floating browser icons
Preferences/Tools/Web Browsers/Show browser popup in the editor = False