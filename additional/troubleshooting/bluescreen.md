# PC BLUESCREEN

Fix for bluescreens (BSOD) occurring during or after spoofing.

---

## 🔍 Common Causes

- 🔒 Secure Boot still enabled
- 🛡️ TPM/fTPM enabled (for non-Valorant games)
- ⚙️ Driver conflicts
- 💾 Disk/RAM hardware issues
- 🔧 Incorrect BIOS settings

---

## ✅ Solution 1: Check BIOS Settings

### Disable Secure Boot

1. Enter BIOS (Del/F2 during boot)
2. Find **Security** → **Secure Boot**
3. Set to **DISABLED**
4. Save & Exit (F10)

### Disable TPM (Non-Valorant)

1. In BIOS → **Security** or **Advanced**
2. Find **TPM Device** or **fTPM**
3. Set to **DISABLED**
4. Save & Exit

> ⚠️ **For Valorant:** Keep TPM ENABLED, use FTPM spoof instead!

---

## ✅ Solution 2: Fresh Windows Install

If bluescreens persist:

1. **Backup important data**
2. **Create Windows USB**
3. **Boot from USB**
4. **Delete ALL partitions** during install
5. **Clean install** Windows
6. **Configure BIOS** properly before spoofing

---

## ✅ Solution 3: Check Hardware

### Run Memory Test

1. Search "Windows Memory Diagnostic"
2. Select "Restart now and check for problems"
3. Wait for test to complete
4. Check results after restart

### Check Disk Health

Open Command Prompt as Admin:
```cmd
chkdsk C: /f /r
```

Restart when prompted.

---

## 📋 BIOS Settings Checklist

Ensure these are set correctly:

- [ ] Secure Boot: **DISABLED**
- [ ] TPM/fTPM: **DISABLED** (except Valorant)
- [ ] Fast Boot: **DISABLED**
- [ ] Virtualization (VT-x/SVM): **DISABLED**
- [ ] CSM: **ENABLED**

---

## 🆘 Still Getting Bluescreens?

1. **Note the error code** (e.g., "DRIVER_IRQL_NOT_LESS_OR_EQUAL")
2. **Screenshot** the bluescreen if possible
3. **Check** Windows Event Viewer for details
4. **Contact support** with error information

---

## 🔍 Understanding Bluescreen Codes

Common codes related to spoofing:

- `DRIVER_IRQL_NOT_LESS_OR_EQUAL` → Driver conflict
- `SYSTEM_SERVICE_EXCEPTION` → Service/driver issue  
- `KERNEL_SECURITY_CHECK_FAILURE` → Secure Boot/TPM issue
- `PAGE_FAULT_IN_NONPAGED_AREA` → Memory/driver issue

---

**Related:**
- [BIOS Configuration](../../spoofer-setup/bios-config.md)
- [Windows Reinstall](../../spoofer-setup/windows-reinstall/README.md)
