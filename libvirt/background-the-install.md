# Background The Install

For _--noautoconsole_:

> Note, virt-install exits quickly when this option is specified. If
> your command requested a multistep install, like --cdrom or
> --location, after the install phase is complete the VM will be
> shutoff, regardless of whether a reboot was requested in the VM. If
> you want the VM to be rebooted, virt-install must remain running. You
> can use '--wait' to keep virt-install alive even if --noautoconsole is
> specified.

```bash
$ virt-install \
--name myhost \
--hvm \
--vcpus 2 \
--memory 4096 \
--disk path=/var/lib/libvirt/images/myhost.img,size=10 \
--network network=dev \
--graphics=none \
--location /var/lib/libvirt/images/RHEL.iso \
--extra-args console=ttyS0 \
--extra-args='inst.ks=file:kickstart.cfg' \
--initrd-inject=/tmp/kickstart.cfg \
--wait=-1 \
--noautoconsole &
```
