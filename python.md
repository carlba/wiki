## Detect if script is being debugged or running from CLI
```python
def is_debugging():
    return 'pydevd' in sys.modules
```

## Get number of occurrences of word in string

```python
def count_occurence_of_word_in_string(word, string):
    re.split('\W', string).count('dog')
```