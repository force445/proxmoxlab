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
![Alt text](https://github.com/force445/proxmoxlab/blob/main/proxmox-create-vm-iso.jpg)
