QEMU
===


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
