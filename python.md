# Python

## HowTo

### Detect if script is being debugged or running from CLI

```python
def is_debugging():
    return 'pydevd' in sys.modules
```

### Get number of occurrences of word in string

```python
def count_occurence_of_word_in_string(word, string):
    re.split('\W', string).count('dog')
```

## Projects

### Initialize Python Project

[cookiecutter](https://cookiecutter.readthedocs.io/en/latest)

```bash
cookiecutter https://github.com/carlba/cookiecutter-pypackage
```

### Dockerize Python Project

https://docs.docker.com/compose/gettingstarted/

```dockerfile
FROM python:3
ADD . /app
WORKDIR /app
RUN pip install -r requirements.txt
RUN pip install -e .
CMD route53dyn
```

```bash
docker build -t route53dyn
```
