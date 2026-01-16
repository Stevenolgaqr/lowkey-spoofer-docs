# BIOS Configurations

Essential BIOS settings for optimal spoofer performance and compatibility.

---

## 🔓 Accessing BIOS

Common keys to press during boot:

| Brand | BIOS Key |
|-------|----------|
| **ASUS** | Del or F2 |
| **MSI** | Del |
| **Gigabyte** | Del |
| **ASRock** | Del or F2 |
| **HP** | F10 or Esc |
| **Dell** | F2 or F12 |
| **Lenovo** | F1 or F2 |

**💡 Tip:** Press the key repeatedly as soon as you power on the PC!

**Video Guide:** [How to easily boot into BIOS](https://youtu.be/mb9X9_NNxuo?si)

---

## ⚙️ Required BIOS Settings

### 1. TPM/fTPM (Trusted Platform Module)

> ⚠️ **IMPORTANT**: Disable for ALL games EXCEPT Valorant!

**Location:** `Security → TPM Device → DISABLED`

**Variations:**
- **ASUS**: Advanced → Trusted Computing → TPM Device Selection → Disabled
- **MSI**: Security → Trusted Computing → Security Device Support → Disable
- **Gigabyte**: Peripherals → Trusted Computing → Security Device Support → Disable
- **ASRock**: Security → Intel Platform Trust Technology → Disabled

**For Valorant:** Keep TPM **ENABLED** (you'll use permanent FTPM spoof instead)

---

### 2. Secure Boot

**Location:** `Security → Secure Boot → DISABLED`

**Variations:**
- **ASUS**: Boot → Secure Boot → OS Type → Other OS
- **MSI**: Settings → Security → Secure Boot → Disabled
- **Gigabyte**: BIOS Features → Secure Boot → Disabled
- **ASRock**: Security → Secure Boot → Disabled

---

### 3. Fast Boot

**Location:** `Boot → Fast Boot → DISABLED`

This ensures all drivers load properly on startup.

---

### 4. Virtualization (VT-x / SVM)

**Location:** `Advanced → CPU Configuration → Virtualization → DISABLED`

**AMD Systems:** SVM Mode → Disabled  
**Intel Systems:** Intel VT-x → Disabled

---

### 5. WiFi & Bluetooth [REQUIRED]

> ⚠️ **CRITICAL**: MUST be disabled if you use Ethernet!

**Only do this step if you have WiFi/Bluetooth available, otherwise skip it.**

**If your PC has WiFi enabled, it MUST be disabled via BIOS!** If you solely rely on WiFi, you will need to purchase a new WiFi adapter or use Ethernet!

**Locations:**
- **ASUS**: Advanced → Onboard Devices Config → WiFi/WLAN & Bluetooth → Disabled
- **MSI**: Advanced → Integrated Peripherals → WiFi/WLAN & Bluetooth → Disabled
- **Gigabyte**: Advanced/Peripherals → WiFi/WLAN & Bluetooth → Disabled
- **ASRock**: Advanced → Chipset Configuration → WiFi/WLAN & Bluetooth → Disabled

**Verification:** After disabling, MAC address should show **"N/A HARDWARE"**

---

### 6. CSM (Compatibility Support Module)

**Location:** `Boot → CSM → ENABLED`

Helps with driver compatibility.

---

## 📸 Video Guides - Disable TPM

### ASUS
[Watch: ASUS TPM Disable Guide](https://streamable.com/sicp16)
- **INTEL**: 00:00 timestamp
- **AMD**: Starts at 01:20

### MSI
[Watch: MSI TPM Disable Guide](https://streamable.com/n7q3dk)
- **INTEL**: 00:00 timestamp  
- **AMD**: Starts at 01:05

### ASRock
[Watch: ASRock TPM Disable Guide](https://streamable.com/ec8u3s)
- **INTEL**: 00:00 timestamp
- **AMD**: Starts at 01:35

### Gigabyte
[Watch: Gigabyte TPM Disable Guide](https://streamable.com/1qhn35)
- **INTEL**: 00:00 timestamp
- **AMD**: Starts at 01:50

---

## ✅ Verify Settings in Windows

After configuring BIOS and installing Windows, verify settings:

### Check Secure Boot Status
Open PowerShell as Administrator:
```powershell
Confirm-SecureBootUEFI
```
**Expected result:** `False` or Error (meaning it's disabled) ✅

### Check TPM Status
```powershell
Get-Tpm
```
**Expected result:** `TpmPresent: False` or disabled ✅

### Check Virtualization
```powershell
Get-ComputerInfo | Select-Object HyperVRequirementVirtualizationFirmwareEnabled
```
**Expected result:** `False` ✅

---

## 📋 Quick Checklist

Before leaving BIOS, confirm:

- [ ] **TPM/fTPM** - Disabled (except Valorant)
- [ ] **Secure Boot** - Disabled
- [ ] **Fast Boot** - Disabled
- [ ] **Virtualization** - Disabled
- [ ] **WiFi/Bluetooth** - Disabled (if using Ethernet)
- [ ] **Settings Saved** - Press F10 and confirm

---

**Next Step:** [Disable Windows Defender](disable-defender.md) →
