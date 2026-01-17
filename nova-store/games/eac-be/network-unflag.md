# Network Unflag

Press Win + R, Type ncpa.cpl and click OK. (Now, Disable everything but Ethernet)

Right-click on the connection that you are using and click on Properties.

Change your setings so they will look like this:

{% hint style="info" %}
Only IPv4 should be checked
{% endhint %}

Press Win + R, Type devmgmt.msc and click OK. (Now, Press on the arrow of Network Adapters)

Right-click on the connection that you are using and click on Properties.

Go To the Advanced Tab.

Search For these settings and set them up as follows (If some settings are missing, skip them):

```
Advanced EEE - Disabled
Network Address - Not Present
ARP Offload - Disabled
Flow Control - Disabled
IPv4 Checksum Offload - Disabled
Large Send Offload v2 (IPv6) - Disabled
TCP Checksum Offload (IPv6) - Disabled
UDP Checksum Offload (IPv6) - Disabled
```

Open CMD as Admin and type these Commands 1 by 1 in order.

```bash
ipconfig /flushdns
ipconfig /registerdns
ipconfig /release
ipconfig /renew
netsh winsock reset
```

**Restart PC Again**

Open CMD again as Admin and do these commands.

```bash
arp -d
netsh interface IP delete arpcache
```

**Restart PC Again**
