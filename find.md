# Usage

## Find all files with names matching pattern in current dir and delete them

```bash
find $PWD -name "*~" -exec rm -f {} \;
```