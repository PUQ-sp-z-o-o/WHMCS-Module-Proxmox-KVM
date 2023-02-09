# 6c. Email Template (puqProxmoxKVM Reset password)

#####  [Order now](https://panel.puqcloud.com/index.php?rp=/store/whmcs-module-proxmox-kvm) | [Dowload](https://download.puqcloud.com/WHMCS/servers/PUQ_WHMCS-Proxmox-KVM/) | [FAQ](https://faq.puqcloud.com/)

##### Create an email template for customer notifications.

```
System Settings->Email Templates->Create New Email Template
```

- **Email Type:** Product/service
- **Unique Name:** puqProxmoxKVM Reset password

[![image-1662468737310.png](https://doc.puq.info/uploads/images/gallery/2022-09/scaled-1680-/image-1662468737310.png)](https://doc.puq.info/uploads/images/gallery/2022-09/image-1662468737310.png)

**Subject:**

```
Reset password is ready
```

**Body:**

```
Dear {$client_name},

Password reset successful.

IP address: {$service_dedicated_ip} or {$service_domain}
Username: {$service_username}
Password: {$service_password}


Thank you for choosing us.

{$signature}
```

[![image-1662468808462.png](https://doc.puq.info/uploads/images/gallery/2022-09/scaled-1680-/image-1662468808462.png)](https://doc.puq.info/uploads/images/gallery/2022-09/image-1662468808462.png)