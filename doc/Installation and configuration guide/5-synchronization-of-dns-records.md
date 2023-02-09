# 5. Synchronization of DNS records

#####  [Order now](https://panel.puqcloud.com/index.php?rp=/store/whmcs-module-proxmox-kvm) | [Dowload](https://download.puqcloud.com/WHMCS/servers/PUQ_WHMCS-Proxmox-KVM/) | [FAQ](https://faq.puqcloud.com/)

For your convenience, we have prepared a mechanism that generates basic domain entries for newly created servers.

Setting these entries is not necessary for the correct operation and use of the service.

<p class="callout warning">In this version of the module, we do not have integration of procedures and mechanisms for synchronizing DNS records with various DNS servers. The module returns all IP addresses and DNS records as json using an http request. You need to do the integration with your DNS server yourself.</p>

<p class="callout success">We want to introduce automatic integration of DNS records into popular services and DNS servers. But we don't know where to start. You can help us with this. Please visit our forum and post your needs. We will definitely try to implement them in future versions.  
[https://forum.puqcloud.com/](https://panel.puqcloud.com/link.php?id=9)</p>

##### How it works

In order to get all IP addresses and DNS records, you need to send a GET request.

```
https://<WHMCS-SERVER>/modules/servers/puqProxmoxKVM/lib/dns/dns.php
```

Answer:

```JSON
[
   {
      "forward" : "vlan-1-4779.vps.uuq.pl",
      "ip" : "192.168.0.2",
      "reverse" : "mail.uuq.pl"
   },
   {
      "forward" : "vps-1-4780.vps.uuq.pl",
      "ip" : "192.168.0.3",
      "reverse" : "test.vps.uuq.pl"
   },
   {
      "forward" : "vlan-1-4781.vps.uuq.pl",
      "ip" : "192.168.0.4",
      "reverse" : "blabla.vps.uuq.pl"
   }
]
```

<p class="callout info">The script does not return entries that contain errors or are empty.</p>

With this information, you can import DNS records into your DNS server.

##### Security

For unauthorized access in the directory with the dns.php file, there is a .htaccess file in which you can allow access to specific IPs.

##### .htaccess file example

```
order deny,allow
deny from all
allow from <allowed_IP_address>
```