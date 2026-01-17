# Flashing Bios (VALORANT)

{% hint style="danger" %}
**FOR VALORANT ONLY!**

DO NOT do this for other games unless you know what you're doing!
{% endhint %}

***

## Why Flash BIOS?

Valorant's **Vanguard** anti-cheat tracks BIOS-level identifiers. Flashing BIOS changes these identifiers.

***

## Requirements:

{% hint style="warning" %}
**CRITICAL REQUIREMENTS:**
{% endhint %}

* ⚡ **UPS or stable power** - Power loss = bricked motherboard!
* 💾 **USB drive** (4GB+)
* 🔧 **BIOS file** for your exact motherboard model
* 📱 **Phone** to read instructions during process

***

## Step 1: Find Your Motherboard

Open Command Prompt:

```cmd
wmic baseboard get product,manufacturer,version
```

Example output:
```
Manufacturer: ASUS
Product: ROG STRIX B550-F
Version: Rev X.0x
```

📸 **Take a screenshot!** You'll need this info.

***

## Step 2: Download BIOS File

### ASUS:
1. Go to [asus.com/support](https://www.asus.com/support/)
2. Search your motherboard model
3. Go to **Driver & Utility** section
4. Download latest **BIOS** file (.CAP or .ZIP)

### MSI:
1. Go to [msi.com/support](https://www.msi.com/support)
2. Search your board
3. **BIOS** tab
4. Download latest version

### Gigabyte:
1. Go to [gigabyte.com/support](https://www.gigabyte.com/support)
2. Search your board
3. **BIOS** section
4. Download latest

### ASRock:
1. Go to [asrock.com/support](https://www.asrock.com/support/)
2. Search your model
3. **BIOS** tab
4. Download

***

## Step 3: Prepare USB

1. Insert USB drive
2. **Format as FAT32**
3. Copy BIOS file to USB
4. **Keep original filename!**

***

## Step 4: Flash BIOS

{% hint style="danger" %}
**⚠️ DO NOT:**
* Turn off PC during flash
* Unplug power
* Remove USB
* Press any keys
{% endhint %}

### Enter BIOS:

1. Restart PC
2. Press **Del** or **F2** repeatedly

### Flash Process:

| Brand | Tool | Location |
|-------|------|----------|
| **ASUS** | EZ Flash 3 | Advanced menu |
| **MSI** | M-Flash | Settings menu |
| **Gigabyte** | Q-Flash | BIOS menu |
| **ASRock** | Instant Flash | Advanced menu |

### Steps:

1. Find flash utility in BIOS
2. Select BIOS file from USB
3. Confirm flash
4. **Wait 3-5 minutes** ⏳
5. PC restarts automatically

***

## Step 5: Verify

After restart, enter BIOS again:
* Check BIOS version matches what you flashed

Or in Windows:
```cmd
wmic bios get smbiosbiosversion
```

***

{% hint style="success" %}
**BIOS Flashed!** Now continue with spoofer setup.
{% endhint %}
