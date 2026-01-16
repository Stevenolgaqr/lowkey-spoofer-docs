# Download Ethernet Drivers

> ⚠️ **ONLY FOR PEOPLE WITH ETHERNET (NO WIFI)**

Install network drivers BEFORE connecting to the internet to prevent Windows from installing unwanted drivers and updates.

---

## 🔍 Why Download Drivers First?

Installing drivers offline prevents:
- ❌ Windows Update from interfering
- ❌ Automatic installation of wrong drivers
- ❌ Windows Defender from re-enabling
- ❌ Unwanted system changes

**Always install drivers BEFORE connecting to internet!**

---

## Step 1: Identify Your Network Adapter

### Method A: Check Device Manager (Before Reinstall)

1. Press `Win + X` → **Device Manager**
2. Expand **"Network adapters"**
3. Note down the exact model name
4. Take a photo with your phone! 📸

### Method B: Command Line

Open Command Prompt:
```cmd
wmic nic get name, manufacturer
```

Example output:
```
Intel(R) Ethernet Connection I219-V
Realtek PCIe GbE Family Controller
```

### Method C: Check Motherboard Manual

Your motherboard manual lists the network adapter model.

---

## Step 2: Download Drivers

Download drivers on a **different PC** or **before reinstalling Windows**, and save them to a USB drive.

### 🔷 Intel Ethernet

**Website:** [intel.com/network](https://www.intel.com/content/www/us/en/download-center/home.html)

**Common Intel Models:**
- Intel I211
- Intel I219-V
- Intel I225-V
- Intel I226-V

**Download:**
1. Go to Intel Download Center
2. Search for your model (e.g., "I219-V")
3. Download **"Network Adapter Driver for Windows 10"**
4. Choose **standalone installer** (not exe that requires internet)

**Direct Link:** [Intel Ethernet Adapter Complete Driver Pack](https://www.intel.com/content/www/us/en/download/18293/intel-network-adapter-driver-for-windows-10.html)

---

### 🟠 Realtek Ethernet

**Website:** [realtek.com](https://www.realtek.com/en/downloads)

**Common Realtek Models:**
- RTL8111
- RTL8125
- RTL8152
- RTL8153

**Download:**
1. Go to Realtek Downloads
2. Select **"Network Interface Controllers"**
3. Choose **"PCIe GBE Family Controller"**
4. Download latest driver for Windows 10/11

**Direct Link:** [Realtek PCIe GBE Ethernet Family Controller Drivers](https://www.realtek.com/en/component/zoo/category/network-interface-controllers-10-100-1000m-gigabit-ethernet-pci-express-software)

---

### 🔴 Killer Networks (Intel-based)

**Website:** [killernetworking.com](https://www.killernetworking.com/driver-downloads)

**Common Killer Models:**
- Killer E2500
- Killer E3000
- Killer E3100

**Download:**
1. Go to Killer Networking Downloads
2. Select your Killer adapter model
3. Download **"Killer Performance Suite"** or standalone driver

---

### 🟣 Aquantia / Marvell

**Website:** [marvell.com](https://www.marvell.com/support/downloads.html)

Used in some high-end motherboards (ASUS ROG, MSI, etc.)

---

### 🔵 Broadcom

Less common, but check your motherboard manufacturer's website.

---

## Step 3: Save to USB Drive

1. **Insert USB drive**
2. **Create folder** called `Drivers`
3. **Copy driver installer** to the folder
4. **Safely eject** USB drive

---

## Step 4: Install Drivers (After Windows Reinstall)

### Before Connecting to Internet:

1. ✅ **Do NOT connect** Ethernet cable yet
2. ✅ **Keep WiFi disabled**
3. ✅ **Windows should show** "No internet connection" - this is good!

### Installation Steps:

1. **Insert USB drive** with drivers
2. **Run driver installer** as Administrator
3. **Follow installation wizard**
4. **Choose** "Complete" or "Typical" installation
5. **Restart PC** if prompted

### After Installation:

1. **Connect Ethernet cable**
2. **Verify connection** in Network settings
3. Internet should work now! ✅

---

## ✅ Verify Driver Installation

Open Command Prompt:
```cmd
ipconfig /all
```

You should see your Ethernet adapter listed with:
- Description (adapter name)
- Physical Address (MAC)
- IPv4 Address
- Default Gateway

**Or use PowerShell:**
```powershell
Get-NetAdapter | Select-Object Name, InterfaceDescription, Status
```

**Expected result:** Status should be **"Up"** ✅

---

## 🚨 Troubleshooting

### Driver Not Installing
- Run installer as Administrator
- Disable any antivirus temporarily
- Try compatibility mode (right-click → Properties → Compatibility)

### No Internet After Installing
- Check if Ethernet cable is plugged in properly
- Try different Ethernet port on router
- Restart router and PC
- Check Device Manager for yellow exclamation marks

### Wrong Driver Installed
- Uninstall from Device Manager
- Restart PC
- Install correct driver

---

## 📋 Checklist

Before moving on:

- [ ] Drivers downloaded to USB drive
- [ ] Windows reinstalled (if applicable)
- [ ] Internet still disconnected
- [ ] Drivers installed from USB
- [ ] PC restarted
- [ ] Ethernet cable connected
- [ ] Internet working

---

**Next Step:** [😊 IMPORTANT NOTES](important-notes.md) →
