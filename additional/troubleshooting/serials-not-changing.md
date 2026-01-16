# SERIALS NOT CHANGING

Instructions on how to fix the common issue of serials not changing after spoofing.

---

## 🔍 Diagnosis

After spoofing and restarting, check Device Info tab:
- ❌ **Red serials** = Not changed
- ✅ **Green serials** = Successfully changed
- ⚪ **White serials** in device tab = Normal (ignore these)

---

## 🛠️ Solution Steps

### Step 1: Verify Antivirus is Disabled

**Make sure ALL antivirus is disabled, even after PC restart!**

1. Open Windows Security
2. Check if Real-Time Protection is OFF
3. Verify Tamper Protection is OFF
4. Check after restart - it should STAY disabled

If it re-enables:
- Use dControl tool again
- Add registry disable
- Disable Windows Update service

---

### Step 2: Disable TPM/Trusted Computing Module

**Try disabling TPM in BIOS:**

### ASUS
📹 [Watch: ASUS TPM Disable](https://streamable.com/sicp16)
- **INTEL**: 00:00
- **AMD**: Starts 01:20

### MSI
📹 [Watch: MSI TPM Disable](https://streamable.com/n7q3dk)
- **INTEL**: 00:00
- **AMD**: Starts 01:05

### ASRock
📹 [Watch: ASRock TPM Disable](https://streamable.com/ec8u3s)
- **INTEL**: 00:00
- **AMD**: Starts 01:35

### Gigabyte
📹 [Watch: Gigabyte TPM Disable](https://streamable.com/1qhn35)
- **INTEL**: 00:00
- **AMD**: Starts 01:50

After disabling TPM, **restart** and run spoofer again.

---

### Step 3: Don't Use Edge Browser

**Don't use Edge as default browser!**

Install and set as default:
- ✅ **Brave Browser** (recommended)
- ✅ Chrome
- ✅ Firefox

**How to change:**
1. Settings → Default Apps
2. Set Brave/Chrome as default browser

---

### Step 4: Use VPN + Spoof Again

If nothing above helped:

1. **Connect to any VPN** (free or paid)
2. **Run spoofer** again
3. **Restart PC**
4. **Check serials** - should be green now!

**Why this works:** Bypasses potential ISP/network blocks

---

## ✅ Verification

After trying fixes:

1. Open Lowkey Loader
2. Go to "Device Info"
3. Check serials:
   - ✅ All should be **GREEN**
   - ⚪ White in device tab is normal
   - ❌ If still red, repeat steps

---

## 🆘 Still Not Working?

If serials still won't change:

1. **Completely reinstall Windows** (with disk format)
2. **Flash BIOS** (if you haven't already)
3. **Try RAID installation** method instead
4. **Contact support** with screenshots

---

**Related Guides:**
- [BIOS Configuration](../../spoofer-setup/bios-config.md)
- [Disable Windows Defender](../../spoofer-setup/disable-defender.md)
- [Loader Crash Fix](loader-crash.md)
