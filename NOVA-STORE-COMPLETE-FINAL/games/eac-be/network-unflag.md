# 7️⃣Network Unflag

Clean your network footprint to prevent tracking.

***

## Step 1: Disable Unused Adapters

1. Press **Win + R**
2. Type: `ncpa.cpl`
3. Press **Enter**

**Disable everything EXCEPT Ethernet:**

* ❌ WiFi
* ❌ Bluetooth  
* ❌ Virtual adapters (VirtualBox, VMware, etc.)
* ✅ Ethernet ONLY

{% hint style="info" %}
Right-click adapter → **Disable**
{% endhint %}

***

## Step 2: Configure Ethernet Properties

![Ethernet Properties](../../images/network/ethernet-properties.png)

**Right-click Ethernet → Properties**

### ONLY IPv4 Should Be Checked ✅

**Disable all others:**
* ❌ Internet Protocol Version 6 (TCP/IPv6)
* ❌ Client for Microsoft Networks
* ❌ File and Printer Sharing
* ❌ QoS Packet Scheduler
* ❌ Link-Layer Topology Discovery
* ❌ VirtualBox NDIS6 Bridged Networking Driver
* ❌ Everything else!

***

## Step 3: Advanced Settings

**Click "Configure" → Advanced Tab**

Set these settings:

| Setting | Value |
|---------|-------|
| **Advanced EEE** | Disabled |
| **Network Address** | Not Present |
| **ARP Offload** | Disabled |
| **Flow Control** | Disabled |
| **IPv4 Checksum Offload** | Disabled |
| **Large Send Offload v2 (IPv6)** | Disabled |
| **TCP Checksum Offload (IPv6)** | Disabled |
| **UDP Checksum Offload (IPv6)** | Disabled |

{% hint style="info" %}
**Can't find a setting?** Skip it - not all adapters have all options
{% endhint %}

***

## Step 4: Clean DNS & Network Stack

**Open CMD as Administrator**

Run these commands **ONE BY ONE:**

```cmd
ipconfig /flushdns
ipconfig /registerdns
ipconfig /release
ipconfig /renew
netsh winsock reset
```

{% hint style="warning" %}
**RESTART PC AFTER THIS!** 🔄
{% endhint %}

***

## Step 5: Clear ARP Cache

**After restart, open CMD as Admin again:**

```cmd
arp -d
netsh interface IP delete arpcache
```

{% hint style="warning" %}
**RESTART PC AGAIN!** 🔄
{% endhint %}

***

## Step 6: Verify

**Open CMD:**

```cmd
ipconfig /all
```

Check for:
* ✅ MAC Address changed (if you did MAC spoof)
* ✅ IPv4 address only
* ✅ NO IPv6

***

{% hint style="success" %}
**Network Unflagged!** Continue to Make New Account
{% endhint %}
