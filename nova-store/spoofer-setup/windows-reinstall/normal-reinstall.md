# Normal Reinstallation + Disk Bypass

### Requirements:

* USB 8GB+
* Windows 10/11 ISO
* 30-60 minutes

### Steps:

1. Create bootable USB (Rufus or Media Creation Tool)
2. Boot from USB (F12/F8/Del)
3. **DELETE ALL PARTITIONS** (Important!)
4. Install Windows on unallocated space
5. Setup Windows (offline account, disable privacy)
6. Change Disk Serial using diskpart

### Change Disk Serial:

```bash
diskpart
list disk
select disk 0
uniqueid disk ID=RANDOM1234
```

{% hint style="warning" %}
Use random serial numbers!
{% endhint %}
