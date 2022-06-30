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

(\<device-tree>.dtb for **TEK3-NVJETSON**: tegra210-tek3-nvjetson-a1.dtb)

* Copy new device-tree to device

Copy **Linux_for_Tegra/sources/kernel/kernel-4.9/arch/arm64/boot/dts/\<device-tree>.dtb**

to device 
```
/boot/
```
