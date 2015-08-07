# Ubuntu Screen Resolution in a Hyper-V VM

Steps:

* Open Terminal
* Type: `sudo vi /etc/default/grub`
* Find the line starting with `GRUB_CMDLINE_LINUX_DEFAULT`, and add `video=hyperv_fb:1920x1080"
* Write the changes and quit vi.
* Run: sudo update-grub
* Reboot the virtual machine

Credits:
http://blogs.msdn.com/b/virtual_pc_guy/archive/2014/09/19/changing-ubuntu-screen-resolution-in-a-hyper-v-vm.aspx
