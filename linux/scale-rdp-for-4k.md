# Scale 4k For RDP

We have wayland scaled to 200% on a 4k monitor, using the values below,
RDP will match the screen of the monitor.

```bash
$ xfreerdp  /smart-sizing:3840x2160 /size:1920x1080
```
