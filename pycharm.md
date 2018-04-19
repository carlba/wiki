# Installation

# Usage

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


| Key combination         | Meaning                              |
|:------------------------|:-------------------------------------|
| CMD + K                 | Commit to VCS.                       |


## Fix Skiptest error

_jb_runner_tools.py

``` python
class NewTeamcityServiceMessages(_old_service_messages):
    _latest_subtest_result = None
    
    def message(self, messageName, **properties):
        if messageName in set(["enteredTheMatrix", "testCount", "testIgnored"]):
```




## Themes

[Zenburn](https://github.com/darvin/JetBrains-ZenBurn)

# Configuration

## Hide the floating browser icons
Preferences/Tools/Web Browsers/Show browser popup in the editor = False
