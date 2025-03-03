# How To Mount HFS

- [bindfs](https://askubuntu.com/questions/100167/how-to-mount-hfs-drive-and-ignore-permissions)

```bash
$ yum install bindfs
$ bindfs  -u $(id -u) -g $(id -g) /run/media/$(id -u)/$mydisk/ /mnt/
```
