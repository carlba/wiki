# Usage

## Create a properly aligned ``GPT`` partion

```bash
sudo parted -a optimal /dev/sdh mkpart primary 0% 100%
```
http://unix.stackexchange.com/questions/38164/create-partition-aligned-using-parted/49274

## Create partition

```bash
sudo mkfs.ext4 -m 2 -T largefile4 /dev/sde1
```

## Label a disk

```bash
sudo e2label /dev/sdh1 lannister
```