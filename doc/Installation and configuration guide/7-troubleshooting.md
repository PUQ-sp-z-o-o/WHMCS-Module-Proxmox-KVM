# 7. Troubleshooting

#####  [Order now](https://puqcloud.com/index.php?rp=/store/whmcs-module-proxmox-kvm) | [Dowload](https://download.puqcloud.com/WHMCS/servers/PUQ_WHMCS-Proxmox-KVM/) | [FAQ](https://faq.puqcloud.com/)

### CRON

In the event that the module does not work properly and activities are not performed, please check the operation of the CRON service in the first place.

Here you can read how the process of provisioning virtual machines works.  
[https://doc.puq.info/books/proxmoxkvm-whmcs-module/page/basic-concepts-and-requirements](https://doc.puq.info/books/proxmoxkvm-whmcs-module/page/basic-concepts-and-requirements)

If your problem is still not resolved, then please run the cron job manually and look at the output in the console.

```shell
/usr/bin/php7.4 -q /WHMCS_DIR/crons/cron.php
```

There must be something like that.

```shell
===========================================
VM_id: 2001
Service_id: 4785
User_id: 1
VMSetDedicatedIp: The local status should be creation
VMClone: The local status should be set_ip
VMSetCpuRam: success
VMSetSystemDiskSize: success
VMSetSystemDiskBandwidth: success
VMSetCreatedAdditionalDisk: success
VMSetAdditionalDiskSize: success
VMSetAdditionalDiskBandwidth: success
VMSetNetwork: success
VMSetFirewall: success
VMSetCloudinit: success
VMStart: success
Remote_status: running
Local_status: ready
ServiceSendEmailVMReady: OK
```
