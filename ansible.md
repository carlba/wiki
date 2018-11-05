## Usage

### Always use synchronize instead of copy for large files or folders
    
```yaml
---
synchronize:
  archive: true
  src: "/Applications/Google Chrome.app/"
  dest: "/Applications/Google Chrome Work.app/"
```

### Ensure that a package is upgraded with pip
```yaml
---
- name: Install python package <package_name>
  pip:
    name: <package_name>
    extra_args: --upgrade
```
