# How To Mount A CIFS Share

```bash
$ mount -t cifs -o vers=2.1,username=$sid,password=$pw,uid=$(id -u),gid=$(id -g) '//example.tld/dfs/$path' /mnt/$mnt
```
