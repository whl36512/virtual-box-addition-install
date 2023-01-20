# Virtualbox Guest Additions Installation

Step 1
- Open a terminal in the guest system
- `yum install kernel kernel-headers kernel-devel gcc make perl`
- `uname -r`  to find kernel version
- `/sbin/rcvboxadd quicksetup 5.14.0-162.6.1.el9_1.0.1.x86_64`  <- this is the kernel version
- Optional: `/sbin/rcvboxadd cleanup`
- `/sbin/rcvboxadd setup`  # this step may report a `ValueErroe`. Ignore it
- `reboot`

Step 2: mount Guest Addition ISO after guest system is up
- in the running guest
- Top Menu -> Devices -> Insert Guest Additions CD Image
- The ISO file will be downloaded automatically if it is not there.
- Reboot the guest system

