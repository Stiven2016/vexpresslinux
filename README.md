cool linux kernels

run on qemu 

qemu-system-arm -M vexpress-a15 -cpu cortex-a15 -m 1024 \
  -kernel zImage \
  -dtb vexpress-v2p-ca15-tc1.dtb \
  -append "root=/dev/mmcblk0p2 rw rootwait" \
  -drive if=sd,file=yourosimg.img,format=raw \
  -net nic -net user





Explanation:
QEMU: Emulator to run different systems.
-M vexpress-a15: Emulates a Versatile Express ARM board.
-cpu cortex-a15: Uses the Cortex-A15 CPU model.
-m 1024: Gives the system 1024 MB of RAM.
-kernel zImage: Specifies the Linux kernel image.
-dtb vexpress-v2p-ca15-tc1.dtb: Device Tree Blob for hardware description.
-append "root=/dev/mmcblk0p2 rw rootwait": Kernel command line parameters.
-drive if=sd,file=yourosimg.img,format=raw: Specifies the root filesystem image (replace yourosimg.img with your own image file).
-net nic -net user: Sets up networking.



