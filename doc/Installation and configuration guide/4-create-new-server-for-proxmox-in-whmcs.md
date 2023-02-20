# 4. Create new server for Proxmox in WHMCS

#####  [Order now](https://puqcloud.com/index.php?rp=/store/whmcs-module-proxmox-kvm) | [Dowload](https://download.puqcloud.com/WHMCS/servers/PUQ_WHMCS-Proxmox-KVM/) | [FAQ](https://faq.puqcloud.com/)

### Preface

For the module to work properly, you must configure the server settings in Your main WHMCS panel. This is the place to set up a proxmox server or proxmox cluster, which will then be used to build KVM machines. Here we define the access data IP ranges and additional settings.

> Attention.  
If you have one server, or you do not use server groups. Van needs to make this server the default. By clicking on it with the mouse. 
>
> **Make this server the active default for new signups**

### Server creation

Login to Your WHMCS panel and create new server Proxmox in WHMCS (*System Settings-&gt;Products/Services-&gt;Servers*)

[![image-1663142713076.png](https://doc.puq.info/uploads/images/gallery/2022-09/scaled-1680-/image-1663142713076.png)](https://doc.puq.info/uploads/images/gallery/2022-09/image-1663142713076.png)

```
System Settings->Servers->Add New Server
```

- Enter the correct **Name** and **Hostname**
- In field Assigned IP Addresses you must enter a list of IP addresses of virtual machines that will be reserved for this server.

### Format to follow in the Assigned IP Addresses field.

To define the available pool of IP addresses, for each available IP number you should enter another line where the data is separated by the "|" separator. Each line with an IP number definition has the following structure:

&lt;bridge&gt;|&lt;vlan\_tag&gt;|&lt;IP\_address&gt;|&lt;net\_mask&gt;|&lt;Gateway&gt;|&lt;DNS1&gt;,&lt;DNS2&gt;

&lt;bridge&gt; - the bridge to which the machine is connected is virtual.  
&lt;vlan\_tag&gt; - vlan which will be installed on the map of the network machine. In case of not using vlan, you need to set 0

### Example:

```
vmbr0|10|192.168.10.2|24|192.168.10.1|8.8.8.8,1.1.1.1
vmbr0|10|192.168.10.3|24|192.168.10.1|8.8.8.8,1.1.1.1
vmbr0|10|192.168.10.4|24|192.168.10.1|8.8.8.8,1.1.1.1
vmbr0|30|192.168.20.2|24|192.168.20.1|8.8.8.8,1.1.1.1
vmbr0|30|192.168.20.3|24|192.168.20.1|8.8.8.8,1.1.1.1
vmbr0|30|192.168.20.4|24|192.168.20.1|8.8.8.8,1.1.1.1
vmbr1|333|172.16.5.2|24|172.16.5.1|8.8.8.8,1.1.1.1
vmbr1|333|172.16.5.3|24|172.16.5.1|8.8.8.8,1.1.1.1
vmbr1|333|172.16.5.4|24|172.16.5.1|8.8.8.8,1.1.1.1
vmbr3|0|10.0.25.2|24|10.0.25.1|10.0.10.10,10.0.10.20
vmbr3|0|10.0.25.3|24|10.0.25.1|10.0.10.10,10.0.10.20
vmbr3|0|10.0.25.4|24|10.0.25.1|10.0.10.10,10.0.10.20
vmbr3|0|10.0.25.5|24|10.0.25.1|10.0.10.10,10.0.10.20
vmbr3|0|10.0.25.6|24|10.0.25.1|10.0.10.10,10.0.10.20
```

[![image-1662467058484.png](https://doc.puq.info/uploads/images/gallery/2022-09/scaled-1680-/image-1662467058484.png)](https://doc.puq.info/uploads/images/gallery/2022-09/image-1662467058484.png)

### Enter the correct data in the username and password field  
  


- In the **Server Details** section, select the "**PUQ Proxmox KVM**" module and enter the correct **username** and **password** for the **Proxmox web interface**.
- To check, click the **"Test connection"** button

>Note that the username is entered with the Proxmox account type (@pam or @pve)

>During operation, the module will automatically fill in the Access Hash field. This field does not need to be completed.

[![image-1662467564570.png](https://doc.puq.info/uploads/images/gallery/2022-09/scaled-1680-/image-1662467564570.png)](https://doc.puq.info/uploads/images/gallery/2022-09/image-1662467564570.png)

>**Attention**  
If you have one server, or you do not use server groups. Van needs to make this server the default. By clicking on it with the mouse.  
>  
>**Make this server the active default for new signups**

[![image-1663408279496.png](https://doc.puq.info/uploads/images/gallery/2022-09/scaled-1680-/image-1663408279496.png)](https://doc.puq.info/uploads/images/gallery/2022-09/image-1663408279496.png)
