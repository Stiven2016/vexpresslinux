
# Cool Linux Kernels

## Run on QEMU

```bash
qemu-system-arm -M vexpress-a15 -cpu cortex-a15 -m 1024 \
-kernel zImage \
-dtb vexpress-v2p-ca15-tc1.dtb \
-append "root=/dev/mmcblk0p2 rw rootwait" \
-drive if=sd,file=yourosimg.img,format=raw \
-net nic -net user -accel tcg -global cpu-clock=1600000000
