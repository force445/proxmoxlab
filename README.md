# Proxmox installation

first prepare your ubuntu system

```bash
sudo apt update
sudo apt full-upgrade
```

## Install virt-manager on Ubuntu

Use this command in a terminal:
```bash
sudo apt install virt-manager
```
Virt-manager will then be available in your applications list. You need to reboot your system to get everything working correctly, if not, you’ll get this error:
```bash
unable to connect to libvirt qemu ///system
```
If you can’t reboot the server, run virt-manager as root with:
```bash
sudo virt-manager
```

## Download Proxmox
Once everything is ready on your system, you can visit the Proxmox website and download the latest ISO file. 
https://proxmox.com/en/downloads/proxmox-virtual-environment/iso

## Create a new virtual machine to host Proxmox
After download ISO file create new vm by doing these steps
-Click on the first icon, “Create a new virtual machine”.

-Keep the default selection, and continue with a “Local install media”.

-Browse to select the ISO file you just downloaded, and select Debian 11,12 in the operating system list.
It won’t find it automatically.
![Alt text](https://github.com/force445/proxmoxlab/blob/main/images/proxmox-create-vm-iso.jpg)

Adjust the memory and CPU settings.
Proxmox requires 2 GB for the main system. Then add as much memory as your additional virtual machines will need.
For example, if you’ll create a virtual machine with 8 GB, you need to create your VM with at least 10 GB.
Same thing for the CPU, 1 is enough for Proxmox, add more depending on your virtual machines requirements.

Create a disk image for the virtual machine (the default 20 GB is fine for Proxmox).
I recommend adding new disks for your VM, instead of keeping everything on the same one.

Name the virtual machine to complete the wizard.

You can now start the virtual machine, and continue the installation like you were doing this directly on your disk.
The following boot menu will show up:
![Alt text](https://github.com/force445/proxmoxlab/blob/main/images/proxmox-boot-menu.jpg)
Select “Install Proxmox VE” and follow the wizard to complete the installation. It will ask you to create an account, make sure to remember it as you’ll need it to access the web interface.
![Alt text](https://github.com/force445/proxmoxlab/blob/main/images/proxmox-install.jpg)
After a few minutes, a success message appears, giving you the web interface URL.
One last reboot is required, so wait a few seconds before trying to access this URL.
![Alt text](https://github.com/force445/proxmoxlab/blob/main/images/proxmox-installed.jpg)

Now you can access the proxmox with its ip through the web browser by use its ip
the username would be root and password is your password
![Alt text](https://github.com/force445/proxmoxlab/blob/main/images/proxmox-running.jpg)
