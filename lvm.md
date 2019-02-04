## Resize a physical disk and expand the lvm VG

```bash
pvresize /dev/"diskname"
lvextend -l +100%FREE -r /dev/mapper/instance_store-lvm
```
