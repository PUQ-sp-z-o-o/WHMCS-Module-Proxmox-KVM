# Description

#####  [Order now](https://panel.puqcloud.com/index.php?rp=/store/whmcs-module-proxmox-kvm) | [Dowload](https://download.puqcloud.com/WHMCS/servers/PUQ_WHMCS-Proxmox-KVM/) | [FAQ](https://faq.puqcloud.com/)

### Preface

The module allows your customers to provision and manage KVM machines using the Proxmox server or Proxmox cluster.

The module allows you to manage virtually all functions available in Proxmox directly from the WHMCS panel without going to the Proxmox panel. This greatly simplifies and facilitates customer account management, improves customer satisfaction and reduces the number of support requests.

To work properly, the module requires a previously configured and working Proxmox server or Proxmox cluster (we have prepared [detailed instructions here](https://doc.puq.info/books/proxmoxkvm-whmcs-module/chapter/installation-and-configuration-guide)) and, apart from other requirements, also the available IP address range

The module is intended for advanced users, because the installation and correct configuration requires knowledge and experience in the management and configuration of servers and the network. Although the instructions are detailed and allow the module to be installed by an intermediate user, we suggest that when installing the module, follow the order in the installation documentation.

For technical reasons, the module will not support LVM-based storage(Due to the fact that they do not use in the cluster as a shared storage).

We provide installation service in two variants: module installation and configuration and full implementation. Please [look here](https://panel.puqcloud.com/link.php?id=27) for details. You can [order service here](https://panel.puqcloud.com/index.php?rp=/store/whmcs-module-proxmox-kvm/whmcs-proxmox-kvm-installation-service).

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


- - - - - -

WHMCS minimal version: 8 +

Minimal Proxmox version: 7 +

### Screenshots

[![image-1662446464115.png](https://doc.puq.info/uploads/images/gallery/2022-09/scaled-1680-/image-1662446464115.png)](https://doc.puq.info/uploads/images/gallery/2022-09/image-1662446464115.png)

[![image-1662446473915.png](https://doc.puq.info/uploads/images/gallery/2022-09/scaled-1680-/image-1662446473915.png)](https://doc.puq.info/uploads/images/gallery/2022-09/image-1662446473915.png)

[![image-1662446479326.png](https://doc.puq.info/uploads/images/gallery/2022-09/scaled-1680-/image-1662446479326.png)](https://doc.puq.info/uploads/images/gallery/2022-09/image-1662446479326.png)

[![image-1662446484561.png](https://doc.puq.info/uploads/images/gallery/2022-09/scaled-1680-/image-1662446484561.png)](https://doc.puq.info/uploads/images/gallery/2022-09/image-1662446484561.png)

[![image-1662446490042.png](https://doc.puq.info/uploads/images/gallery/2022-09/scaled-1680-/image-1662446490042.png)](https://doc.puq.info/uploads/images/gallery/2022-09/image-1662446490042.png)

[![image-1662446499233.png](https://doc.puq.info/uploads/images/gallery/2022-09/scaled-1680-/image-1662446499233.png)](https://doc.puq.info/uploads/images/gallery/2022-09/image-1662446499233.png)

[![image-1662446505531.png](https://doc.puq.info/uploads/images/gallery/2022-09/scaled-1680-/image-1662446505531.png)](https://doc.puq.info/uploads/images/gallery/2022-09/image-1662446505531.png)

[![image-1662460646834.png](https://doc.puq.info/uploads/images/gallery/2022-09/scaled-1680-/image-1662460646834.png)](https://doc.puq.info/uploads/images/gallery/2022-09/image-1662460646834.png)
