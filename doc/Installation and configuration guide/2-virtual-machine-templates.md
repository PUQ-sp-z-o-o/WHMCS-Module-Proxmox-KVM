# 2. Virtual machine templates

#####  [Order now](https://puqcloud.com/index.php?rp=/store/whmcs-module-proxmox-kvm) | [Dowload](https://download.puqcloud.com/WHMCS/servers/PUQ_WHMCS-Proxmox-KVM/) | [FAQ](https://faq.puqcloud.com/)

### Preface

Since the primary purpose of the module is to create and manage virtual KVM machines, the machine templates must be properly prepared and available in the Proxmox panel (standalone server or cluster).

>You can try to use available templates from the Internet (which support *[clud-init](https://cloud-init.io/)* standard) and they should work fine, but we suggest initially using templates that are created according to our standards. We offer a basic set of images for **[download](https://files.puqcloud.com/).**

In order for the automatic installation of the virtual machine to work correctly, You need to prepare virtual machine templates for all operating systems that you want to provide for your customers to choose from.

### The physical state of the virtual machine template

- All parameters of the virtual machine must be less than the smallest package you offer to clients. (cpu, RAM, disk size)
- If you provide a virtual machine with two disks and host these disks on different storages, you need to create these boards in the template of the virtual machine on the necessary data storage, otherwise the additional disk will be created automatically on the same storage as the main disk.
- You need to add a [*cloud-init*](https://cloud-init.io/) disk in order to automatically configure the virtual machine after cloning, your client parameters (network settings, authorization data)

### Virtual machine template software

- Install the desired operating system on the template virtual machine
- *During installation, partitions of the virtual machine disk must be divided so that <span style="text-decoration: underline;">the root partition is the last in the lists</span>.* **This is necessary in order for the automatic change of the system partition to work at the moment when the disk of the virtual machine is enlarged.**
- After installing the operating system, you need to install the [*cloud-init*](https://cloud-init.io/) software suite
    ```
    cloud-initramfs-growroot cloud-init cloud-utils
    ```

### We have prepared templates for popular operating systems.

Templates are in the form of a virtual machine backup.  
In order to use it, you need to download the archive. Then copy it to the Proxmox server and restore the backup.

### Operating system configuration:

- hdd **5 GB** (virtio)
- disabled **swap**
- minimal server installation
- allow the **root** user to connect via ssh
- root password: **puqcloud**
- installed **cloud-initramfs-growroot cloud-init cloud-utils**
- localization and time zone **Europe/Warsaw**
- language ****English****

### Forum

If you need any other operating system or certain parameters, you can discuss it on our forum

[https://forum.puqcloud.com/](https://forum.puqcloud.com/)

>Please note that we provide operating system templates only to demonstrate the functionality of our module.  
YOUR USE OF THESE OPERATING SYSTEMS IS AT YOUR OWN RISK. WE DO NOT GUARANTEE CORRECT OPERATION AND SAFETY. WE DO NOT RECOMMEND TO USE THEM AS OPERATING SYSTEM TEMPLATES FOR YOUR CLIENTS.

### Download prebuild templates

You can download the templates from the links below.

[https://files.puqcloud.com/](https://files.puqcloud.com/)

|Templates | Version  | Version |
| ------------- |:------------------:| -----:|
| **Debian**| [Debian-10](https://files.puqcloud.com/Proxmox_OS_Templates/Debian/Debian-10/vzdump-qemu-1010-2022_09_11-13_43_25.vma.zst) | [Debian-11](https://files.puqcloud.com/Proxmox_OS_Templates/Debian/Debian-11/vzdump-qemu-1011-2022_09_11-13_42_41.vma.zst) |
| **Ubuntu**| [Ubuntu-18](https://files.puqcloud.com/Proxmox_OS_Templates/Ubuntu/Ubuntu-18/vzdump-qemu-1020-2022_09_11-13_41_31.vma.zst) | [Ubuntu-20](https://files.puqcloud.com/Proxmox_OS_Templates/Ubuntu/Ubuntu-20/vzdump-qemu-1021-2022_09_11-13_40_00.vma.zst) |
| **CentOS**| [CentOS-7](https://files.puqcloud.com/Proxmox_OS_Templates/CentOS/CentOS-7/vzdump-qemu-1030-2022_09_11-13_39_13.vma.zst) | [CentOS-8](https://files.puqcloud.com/Proxmox_OS_Templates/CentOS/CentOS-8/vzdump-qemu-1031-2022_09_11-13_38_18.vma.zst) |
| **Proxmox**| [PBS-2.2](http://files.puqcloud.com/Proxmox_OS_Templates/Proxmox/PBS-2-2/vzdump-qemu-1050-2022_09_15-12_53_05.vma.zst) | |
