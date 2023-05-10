# Virtualbox Guest Additions Installation
Set CPU to >=2 to avoid kernel panic when installing Linux


Step 1
- Open a terminal in the guest system
- `uname -r`  to find kernel version
- `yum install kernel-5.14.0-162.6.1.el9_1.0.1.x86_64 kernel-headers-5.14.0-162.6.1.el9_1.0.1.x86_64 kernel-devel-5.14.0-162.6.1.el9_1.0.1.x86_64 gcc make perl`   # must use exact kernel version


Step 2: mount Guest Addition ISO after guest system is up
- in the running guest
- Top Menu -> Devices -> Insert Guest Additions CD Image
- The ISO file will be downloaded automatically if it is not there.
- Reboot the guest system


If step 2 has problem:
Step 3
- `/sbin/rcvboxadd quicksetup 5.14.0-162.6.1.el9_1.0.1.x86_64`  <- this is the kernel version
- Optional: `/sbin/rcvboxadd cleanup`
- `/sbin/rcvboxadd setup`  # this step may report a `ValueErroe`. Ignore it
- `reboot`

