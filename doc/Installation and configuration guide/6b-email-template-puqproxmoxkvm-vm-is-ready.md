# 6b. Email Template (puqProxmoxKVM VM is ready)

#####  [Order now](https://panel.puqcloud.com/index.php?rp=/store/whmcs-module-proxmox-kvm) | [Dowload](https://download.puqcloud.com/WHMCS/servers/PUQ_WHMCS-Proxmox-KVM/) | [FAQ](https://faq.puqcloud.com/)

##### Create an email template for customer notifications.

```
System Settings->Email Templates->Create New Email Template
```

- **Email Type:** Product/service
- **Unique Name:** puqProxmoxKVM VM is ready

[![image-1662468575575.png](https://doc.puq.info/uploads/images/gallery/2022-09/scaled-1680-/image-1662468575575.png)](https://doc.puq.info/uploads/images/gallery/2022-09/image-1662468575575.png)

**Subject:**

<div data-lang="PHP" id="bkmrk-virtual-machine-is-r">```
Virtual Machine is ready
```

</div>**Body:**

```
Dear {$client_name},

Your virtual machine is already ready.
You can connect to it using data.


Product/Service: {$service_product_name}
Payment Method: {$service_payment_method}
Amount: {$service_recurring_amount}
Billing Cycle: {$service_billing_cycle}
Next Due Date: {$service_next_due_date}


IP address: {$service_dedicated_ip} or {$service_domain}
Username: {$service_username}
Password: {$service_password}


Thank you for choosing us.

{$signature}
```

[![image-1662468661245.png](https://doc.puq.info/uploads/images/gallery/2022-09/scaled-1680-/image-1662468661245.png)](https://doc.puq.info/uploads/images/gallery/2022-09/image-1662468661245.png)