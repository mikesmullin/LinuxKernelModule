# Linux Kernel Module Development 101

In this **Hello World** example, which I have tested and confirmed works on my Ubuntu 16.04.4 LTS 4.13.0-37-generic kernel, we make and test the simplest possible binary, which outputs two simple messages to the kernel log file.

### Install Dependencies
```bash
sudo apt-get install build-essential linux-headers-$(uname -r)
```

### Build
```bash
make
```

### Execute
```bash
# Install + run
sudo insmod ./hello.ko 

# Confirm installed
lsmod | grep hello

# Uninstall
sudo rmmod hello

# See log output
dmesg
```

### See also:
- [Linux Device Drivers, Third Edition](https://lwn.net/Kernel/LDD3)
- [Writing a Kernel Module - Part 1: Introduction](http://derekmolloy.ie/writing-a-linux-kernel-module-part-1-introduction)