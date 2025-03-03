# Enable Dnf Automatic Updates

```bash
$ dnf install dnf-automatic
$ sed -ie 's/^apply_updates = .*$/apply_updates = yes/' /etc/dnf/automatic.conf
$ sudo systemctl enable --now dnf-automatic.timer
```
