# TEV-JetsonNano_device-tree
The Jetson Nano device-tree, for JetsonNano TN-TEK 3 series and Nano EVK support.

### Folder location(created by TEV-Jetson_Jetpack_script)
```
<nvidia_folder>/Linux_for_Tegra/sources/hardware/nvidia/platform/t210/porg
```

### Compile device-tree
Please go to kernel source code location to compile device-tree.
``` coffeescript
$ cd <nvidia_folder>/Linux_for_Tegra/sources/kernel/kernel-4.9
$ ./compile_kernel.sh
```

### Take effect
Just re-compile and use the new kernel/ device-tree.
``` coffeescript
$ cd <nvidia_folder>/Linux_for_Tegra/sources/kernel/kernel-4.9/
$ ./compile_kernel.sh
```

* Copy new device-tree to device
(TEK3-NVJETSON: tegra210-tek3-nvjetson-a1.dtb)
Copy **Linux_for_Tegra/sources/kernel/kernel-4.9/arch/arm64/boot/dts/<device-tree>.dtb**

to device 
```
/boot/
```
&nbsp;

* Copy new device-tree to workspace, create new system.img and flash.

Copy **Linux_for_Tegra/sources/kernel/kernel-4.9/arch/arm64/boot/dts/<device-tree>.dtb**

to 
```
<nvidia_folder>/Linux_for_Tegra/rootfs/boot/
```
```coffeescript
$ sudo ./flash.sh jetson-nano-devkit-emmc mmcblk0p1 
```
