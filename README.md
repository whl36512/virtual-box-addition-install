# Virtualbox Guest Additions Installation

Step 1: mount Guest Addition ISO after guest system is up
- in the running guest
- Top Menu -> Devices -> Insert Guest Additions CD Image
- The ISO file will be downloaded automatically if it is not there.

if it reports error `VirtualBox Kernel Headers Not Found`, do step 2

Step 2
- Open a terminal in the guest system
- `yum install kernel kernel-headers kernel-devel gcc`
- `uname -r`  to find kernel version
- `/sbin/rcvboxadd quicksetup 5.14.0-162.6.1.el9_1.0.1.x86_64`  <- this is the kernel version
- Optional: `/sbin/rcvboxadd cleanup`
- `/sbin/rcvboxadd setup`
- `reboot`
