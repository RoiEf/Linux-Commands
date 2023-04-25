# Command set for compiling linux kernel using LLVM in Manjaro

1. Get source files
```
wget https://cdn.kernel.org/pub/linux/kernel/v6.x/linux-6.3.tar.xz
```
2. Extract files
```
tar -xvf linux-6.3.tar.xz
```
3. CD to the extracted directory
```
cd linux-6.3
```
4. Clean the build
```
make mrproper
```
5. Copy the cuttent configuration file
```
zcat /proc/config.gz >> .config
```
6. More configuration
```
make menuconfig
```
7. Compiling the files
```
make LLVM=1 -j4
```
8. Installing the modules
```
sudo make modules_install
```
9. Copy the Kernel file
```
sudo cp -v arch/x86_64/boot/bzImage /boot/vmlinuz-6.3-x86_64
```

### reboot
entering the grub boot menu is using "Esc" key.

Checking the kernel version after reboot
```
cat /proc/version
```

need to continue from initramfs
https://forum.manjaro.org/t/howto-build-your-very-first-custom-kernel/47683
https://www.youtube.com/watch?v=VVunP3yDgm4 time 21:00