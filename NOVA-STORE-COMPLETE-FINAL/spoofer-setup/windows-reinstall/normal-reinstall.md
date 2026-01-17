# Normal Reinstallation + Disk Bypass

### What You Need:

* USB flash drive (8GB minimum)
* Windows 10/11 ISO file
* 30-60 minutes of time
* Backup of important files

***

### Step 1: Create Bootable USB

![USB Media Choice](../../images/windows-install/step1-media-choice.png)

Download and use:
* **Rufus** ([rufus.ie](https://rufus.ie)) - Recommended
* **Microsoft Media Creation Tool** - Official method

![USB Files](../../images/windows-install/step2-usb-files.png)
*Your USB should contain these files after creation*

***

### Step 2: Boot from USB

![Hold Shift + Restart](../../images/windows-install/step3-hold-shift.png)
*Hold SHIFT and click Restart*

![Use a Device](../../images/windows-install/step4-use-device.png)
*Select "Use a device" then choose your USB*

**OR** Press boot key during startup:
* ASUS: F8 or Del
* MSI: F11
* Gigabyte: F12
* HP: F9 or Esc

***

### Step 3: Select Windows Version

![Select Windows](../../images/windows-install/step5-select-windows.png)
*Choose Windows 10 Pro or Windows 11 Pro*

***

### Step 4: Skip Product Key

![Skip Key](../../images/windows-install/step6-skip-product-key.png)
*Click "I don't have a product key"*

***

### Step 5: Custom Installation

![Custom Install](../../images/windows-install/step7-custom-install.png)
*Select "Custom: Install Windows only (advanced)"*

***

### Step 6: DELETE ALL PARTITIONS

![Delete Partitions](../../images/windows-install/step8-delete-partitions.png)

{% hint style="danger" %}
**CRITICAL:** You MUST delete ALL partitions until only "Unallocated Space" remains!
{% endhint %}

1. Select each partition
2. Click "Delete"
3. Confirm
4. Repeat until only unallocated space remains
5. Select unallocated space
6. Click "Next"

***

### Step 7: Installation Process

* Wait 15-30 minutes
* PC will restart several times automatically
* Do NOT remove USB until completely finished

***

### Step 8: Windows Setup - CREATE OFFLINE ACCOUNT

![Offline Account](../../images/windows-install/step9-offline-account.png)
*Click "Offline account" in bottom left*

{% hint style="warning" %}
**DO NOT:**
* Connect to internet during setup
* Sign in with Microsoft account
* Use Edge browser after installation
{% endhint %}

***

### Step 9: Privacy Settings

![Privacy Settings](../../images/windows-install/step10-privacy-settings.png)
*Turn OFF all privacy settings*

***

### Step 10: Change Disk Serial

After Windows is installed, open Command Prompt as Administrator:

```cmd
diskpart
list disk
select disk 0
uniqueid disk
```

You'll see current serial. Now change it:

```cmd
uniqueid disk ID=9F8E7D6C
```

{% hint style="info" %}
Use random alphanumeric characters. Example: `4B7K9M2P` or `8X3V5N1Q`
{% endhint %}

Verify the change:
```cmd
uniqueid disk
exit
```

***

{% hint style="success" %}
**Setup Complete!** Now proceed to BIOS Configuration
{% endhint %}
