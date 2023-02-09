# Virtual machine reinstallation procedure

#####  [Order now](https://panel.puqcloud.com/index.php?rp=/store/whmcs-module-proxmox-kvm) | [Dowload](https://download.puqcloud.com/WHMCS/servers/PUQ_WHMCS-Proxmox-KVM/) | [FAQ](https://faq.puqcloud.com/)

You can reinstall virtual machine at any time if you need to.

On the operating system reinstallation option page the client is given the option to select a new operating system from a list of available ones.  
There is also a warning that all data will be deleted, and the machine will be reinstalled.

<p class="callout info">In order to avoid erroneous reinstallation, we have provided an option that protects against this. The customer needs to manually write the word reinstall in capital letters "REINSTALL"</p>

<p class="callout info">The process begins by removing snapshots and data on the current machine and then starting the installation of a new machine with an already existing IP number, network card MAC address, vlan and ID.</p>

<p class="callout danger">The process permanently deletes data from the machine leaving its backups intact. This gives you the option to restore your machine from a backup to the previous state it was in before reinstallation, even after reinstalling the new system. Please use this option carefully.</p>

[![image-1662456525599.png](https://doc.puq.info/uploads/images/gallery/2022-09/scaled-1680-/image-1662456525599.png)](https://doc.puq.info/uploads/images/gallery/2022-09/image-1662456525599.png)