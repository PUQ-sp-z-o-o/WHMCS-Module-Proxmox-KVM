# WHMCS-Module-Proxmox-KVM
The module allows your customers to provision and manage KVM machines on Proxmox panel with WHMCS system.
# Description

#####  [Order now](https://puqcloud.com/index.php?rp=/store/whmcs-module-proxmox-kvm) | [Dowload](https://download.puqcloud.com/WHMCS/servers/PUQ_WHMCS-Proxmox-KVM/) | [FAQ](https://faq.puqcloud.com/)

### Preface

>Starting with version 1.3 **ProxmoxKVM WHMCS module**, integrates with the **PUQ Customization WHMCS Addon (FREE)** for a thinner tuning of parameters and configurations.
>Check out the PUQ Customization WHMCS Addon
>
>https://doc.puq.info/books/puq-customization-whmcs-addon
>
>https://download.puqcloud.com/WHMCS/addons/PUQ-Customization/

The module allows your customers to provision and manage KVM machines using the Proxmox server or Proxmox cluster.

The module allows you to manage virtually all functions available in Proxmox directly from the WHMCS panel without going to the Proxmox panel. This greatly simplifies and facilitates customer account management, improves customer satisfaction and reduces the number of support requests.

>To work properly, the module requires a previously configured and working Proxmox server or Proxmox cluster (we have prepared [detailed instructions here](https://doc.puq.info/books/proxmoxkvm-whmcs-module/chapter/installation-and-configuration-guide)) and, apart from other requirements, also the available IP address range

>The module is intended for advanced users, because the installation and correct configuration requires knowledge and experience in the management and configuration of servers and the network. Although the instructions are detailed and allow the module to be installed by an intermediate user, we suggest that when installing the module, follow the order in the installation documentation.

>For technical reasons, the module will not support LVM-based storage(Due to the fact that they do not use in the cluster as a shared storage).

>We provide installation service in two variants: module installation and configuration and full implementation. Please [look here](https://panel.puqcloud.com/link.php?id=27) for details. You can [order service here](https://panel.puqcloud.com/index.php?rp=/store/whmcs-module-proxmox-kvm/whmcs-proxmox-kvm-installation-service).

The module, fully installed and correctly implemented in the system, offers the following functionalities.

### Module Functions:

- Automatic creation of a KVM virtual machine
- Service suspend and unsuspend function
- Service termination function. Removes a virtual machine and all dependencies associated with it. Adds a note on the product details page in WHMCS admin panel with the date and IP address that was used by this virtual machine.
- Automatically adds additional disk to a virtual machine if an additional disk is configured in the product configuration (It is possible to provision VM with two separately configured disks - a system booting one and second one).
- Automatically configures virtual machine parameters such as: 
    - the number of CPU processor cores,
    - RAM,
    - disk bandwidth limits such as megabytes per second and the number of I/O operations,
    - network card bandwidth limits.
    - IPv4 and IPv6
    - DNS records forward and reverse
- Automatically selects an available IP address from a list of IP addresses provided during initial module installation and configuration.
- Automatically configures the virtual machine system user and password which is then sent by email to customer.
- Automatically adds rules to the firewall that allow you to avoid spoofing the IP address of the virtual machine.
- Configures the *cloud-init* device to auto-configure the virtual machine.
- Snapshot and backup management. Admin can define options for its clients. *The number of snapshots and backups is configured by additional options to the product, and if it is not specified or set to zero, then the function of snapshots and backup will not be available to the client.*
- Managing forward and reverse zone DNS records - system prepares detailed information with the DNS zone data in the ticket and by providing an endpoint URL address that you can use for automation
- Integrated noVNC WEB console for KVM access
- Implemented the function of reinstalling the operating system with the ability to change the operating system to another.
- The function of resetting the operating system (root) password has been implemented in client and admin panel.
- Statistics on the use of virtual machine resources in the form of graphs (CPU, RAM, disk, network). Real-time metric data are imported from hypervisor.
- Under certain conditions, you can change the virtual machine's identifier to a specific service (the machine with the given identifier must be created on the Proxmox server / cluster and not be connected to any other service). This can be useful when you want to attach existing machines to a module. Machines added in this way may not have all management options
- The function of mount an ISO image to a virtual machine has been implemented.
- We have prepared templates for the most common distributions but You can create additional ones - we provide brief requirements later in this guide.
- Module allows when the virtual machine template has 2 disks that can be stored on different network storages. For example, the system disk of the virtual machine is stored on the fast storage, and an additional disk is stored on the slow storage, designed for backups inside the virtual machine.
- For ISO images, you can use another network storage
- Configurable Option (Backups/Snapshots/CPU/RAM/IPv4/IPv6)


- - - - - -

WHMCS minimal version: 8 +

Minimal Proxmox version: 7 +

### Screenshots

![image](https://github.com/PUQ-sp-z-o-o/WHMCS-Module-Proxmox-KVM/assets/81689153/2efc1e27-0662-48f1-abce-4c20c408fb1c)

![image](https://github.com/PUQ-sp-z-o-o/WHMCS-Module-Proxmox-KVM/assets/81689153/52a2a142-e938-42df-9748-f939748d3ab9)

![image](https://github.com/PUQ-sp-z-o-o/WHMCS-Module-Proxmox-KVM/assets/81689153/a905839b-34fd-4792-8576-185e4f0a6b3c)

![image](https://github.com/PUQ-sp-z-o-o/WHMCS-Module-Proxmox-KVM/assets/81689153/e2ef55be-0691-4c4b-92f5-61b8ce2023b1)

![image](https://github.com/PUQ-sp-z-o-o/WHMCS-Module-Proxmox-KVM/assets/81689153/030eb710-b3e5-4ce7-83ec-7dd2c3dd37ce)

![image](https://github.com/PUQ-sp-z-o-o/WHMCS-Module-Proxmox-KVM/assets/81689153/fd56f743-8d6e-4c58-bbae-f4a04cfc9473)

![image](https://github.com/PUQ-sp-z-o-o/WHMCS-Module-Proxmox-KVM/assets/81689153/48fb7a12-cd3c-48d2-a61f-73e3986558e4)

![image](https://github.com/PUQ-sp-z-o-o/WHMCS-Module-Proxmox-KVM/assets/81689153/865e0a15-58a3-4763-ad6c-58f1e5f4159e)

![image](https://github.com/PUQ-sp-z-o-o/WHMCS-Module-Proxmox-KVM/assets/81689153/d97c7c7d-e7f8-4d1c-a5d9-8add40f98d94)
