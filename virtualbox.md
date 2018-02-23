#Usage

#Mount VDI-file
```
sudo apt-get install qemu-utils
sudo modprobe nbd max_part=16
sudo qemu-nbd -c /dev/nbd0 ~/path/to/my.vdi
sudo partprobe /dev/nbd0
sudo mount /dev/nbd0p1 /mount-target
```

If you have more than one partition, you can access them by number — nbd0p1 is partition 1, nbd0p2 would be partition 2, and so on.

After you finished your investigation, you should unmount VDI image from the network device.

```
$ sudo qemu-nbd -d /dev/nbd0
```