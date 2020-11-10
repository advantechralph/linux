debootstrap
===

References
---

- [DebootstrapChroot](https://wiki.ubuntu.com/DebootstrapChroot)
- [QemuDebootstrap](https://wiki.ubuntu.com/ARM/RootfsFromScratch/QemuDebootstrap)

Command Usage
---

```
$ debootstrap --variant=buildd --arch i386 hardy /var/chroot/hardy http://archive.ubuntu.com/ubuntu/
```

For arm machine

```
$ debootstrap --variant=buildd --arch armhf --foreign bionic ./bionic_armhf http://ports.ubuntu.com/ubuntu-ports
```
