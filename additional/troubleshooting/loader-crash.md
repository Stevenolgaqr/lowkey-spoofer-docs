# LOADER CRASH AFTER INSERT LICENSE

Fix for when the Lowkey Loader crashes after entering license key.

---

## 🔍 Common Causes

- ⚙️ Windows time not synchronized
- 🛡️ Antivirus still running
- 🌐 Internet connection issues
- 💾 Corrupted loader files
- 🔐 Invalid license key format

---

## ✅ Solution: Synchronize Windows Time

### Method 1: Settings UI

1. Open **Settings** (Win + I)
2. Select **Time & Language**
3. Click **Date & Time**
4. Under "Synchronize your clock", click **"Sync Now"**
5. **Wait** for confirmation
6. **Restart** Lowkey Loader

### Method 2: Command Line

Open Command Prompt as Administrator:

```cmd
w32tm /resync
net start w32time
w32tm /resync /force
```

---

## 🛡️ Verify Antivirus is Disabled

Even if you disabled it before, check again:

1. Open Windows Security
2. Virus & threat protection → Manage settings
3. Ensure ALL protections are OFF:
   - ❌ Real-time protection
   - ❌ Cloud-delivered protection
   - ❌ Automatic sample submission
   - ❌ Tamper Protection

---

## 🌐 Check Internet Connection

1. Verify you're connected to internet
2. Try opening a website
3. If using Ethernet, check cable
4. Restart router if needed

---

## 🔄 Redownload Loader

If files are corrupted:

1. **Delete** old Lowkey folder
2. **Download** fresh copy
3. **Extract** to new location
4. **Run** setup scripts again
5. **Launch** and enter license

---

## 🔐 Verify License Format

License key should be:
```
XXXX-XXXX-XXXX-XXXX
```

- Check for typos
- Ensure no extra spaces
- Copy-paste carefully
- Contact seller if invalid

---

## 💻 Run as Administrator

Always ensure:
1. **Right-click** Brave.exe/Loader.exe
2. Select **"Run as Administrator"**
3. Click **Yes** on UAC prompt

---

## 🆘 Still Crashing?

Try these additional steps:

1. **Disable firewall** temporarily
2. **Reinstall Visual C++ Redistributables**
3. **Run Windows Update** and install all updates
4. **Check** Windows Event Viewer for error details
5. **Contact support** with error screenshots

---

**Related:**
- [Serials Not Changing](serials-not-changing.md)
- [PC Bluescreen](bluescreen.md)
