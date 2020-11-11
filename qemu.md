QEMU
===

compile qemu
---

```
$ wget https://download.qemu.org/qemu-2.12.0-rc3.tar.xz
$ tar -xvf qemu-2.12.0-rc3.tar.xz
$ cd qemu-2.12.0-rc3
$ ./configure --target-list=arm-softmmu,aarch64-softmmu
$ make 


```


test 1 
----

```
$ qemu-system-arm \
        -nographic \
        -M sabrelite \
        -m 512 \
        -drive file=rootfs.img,format=raw,id=mycard \
        -device sd-card,drive=mycard \
        -kernel zImage \
        -dtb imx6dl-wise710-a1.dtb \
        -append 'console=ttymxc0 rootfstype=ext4 root=/dev/mmcblk0p0 rw rootwait init=/sbin/init ' \
        -no-reboot


```
