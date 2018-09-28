## Detect if script is being debugged or running from CLI

```python
def is_debugging():
    return 'pydevd' in sys.modules
```