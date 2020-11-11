docker
===

Import rootfs to image repo
---

tar files to standard out and import into image repository 

```
$ tar -C rootfs --numeric-owner -zcpvf - . | docker import - advantechralph/work:wise710a1
```
