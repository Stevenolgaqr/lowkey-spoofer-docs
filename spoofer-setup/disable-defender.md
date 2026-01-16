# Disable Windows Defender

Complete removal of Windows Defender and security features to prevent spoofer interference.

---

## ⚠️ Why Disable Defender?

Windows Defender and other security features will:
- ❌ Block spoofer from running
- ❌ Flag spoofer as malware (false positive)
- ❌ Prevent hardware ID changes
- ❌ Quarantine spoofer files

**All antivirus must be completely disabled for the spoofer to work!**

---

## Method 1: Manual Disable (Simple)

### Step 1: Open Windows Security

1. Press `Win + I` to open Settings
2. Go to **"Update & Security"** → **"Windows Security"**
3. Click **"Virus & threat protection"**

### Step 2: Disable Real-Time Protection

1. Under "Virus & threat protection settings", click **"Manage settings"**
2. Turn OFF:
   - ❌ **Real-time protection**
   - ❌ **Cloud-delivered protection**
   - ❌ **Automatic sample submission**
   - ❌ **Tamper Protection**

### Step 3: Add Exclusions

1. Scroll down to **"Exclusions"**
2. Click **"Add or remove exclusions"**
3. Click **"Add an exclusion"** → **"Folder"**
4. Add: `C:\` (entire C drive)

---

## Method 2: Registry Method (Permanent)

### Using Command Prompt

Open Command Prompt as Administrator and run:

```cmd
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows Defender" /v DisableAntiSpyware /t REG_DWORD /d 1 /f
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows Defender\Real-Time Protection" /v DisableRealtimeMonitoring /t REG_DWORD /d 1 /f
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows Defender\Spynet" /v SpyNetReporting /t REG_DWORD /d 0 /f
sc stop WinDefend
sc config WinDefend start= disabled
```

---

## Method 3: dControl (Recommended)

**Download dControl:** [Download from MEGA](https://mega.nz/file/...)

### Steps:

1. **Download** dControl from the link above
2. **Extract** the ZIP file
3. **Run** `dControl.exe` as Administrator
4. **Click** "Disable Windows Defender"
5. **Restart** your PC

dControl provides a simple interface to completely disable Defender with one click!

---

## Method 4: Batch Script (Advanced)

Create a file called `disable-defender.bat` with this content:

```batch
@echo off
echo ========================================
echo  Disabling Windows Defender
echo ========================================

:: Disable Defender via Registry
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows Defender" /v DisableAntiSpyware /t REG_DWORD /d 1 /f

:: Disable Real-Time Protection
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows Defender\Real-Time Protection" /v DisableRealtimeMonitoring /t REG_DWORD /d 1 /f
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows Defender\Real-Time Protection" /v DisableBehaviorMonitoring /t REG_DWORD /d 1 /f
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows Defender\Real-Time Protection" /v DisableOnAccessProtection /t REG_DWORD /d 1 /f
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows Defender\Real-Time Protection" /v DisableScanOnRealtimeEnable /t REG_DWORD /d 1 /f

:: Disable Cloud Protection
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows Defender\Spynet" /v SpyNetReporting /t REG_DWORD /d 0 /f
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows Defender\Spynet" /v SubmitSamplesConsent /t REG_DWORD /d 2 /f

:: Stop and Disable Windows Defender Service
sc stop WinDefend
sc config WinDefend start= disabled

:: Stop Security Health Service
sc stop SecurityHealthService
sc config SecurityHealthService start= disabled

echo.
echo ========================================
echo  Windows Defender Disabled!
echo  Please RESTART your PC
echo ========================================
pause
```

**Run as Administrator!**

---

## Disable Windows Security Center Notifications

To stop annoying security warnings:

```cmd
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows Defender Security Center\Notifications" /v DisableNotifications /t REG_DWORD /d 1 /f
```

---

## Disable Automatic Updates (Optional)

Prevents Windows Update from re-enabling Defender:

1. Press `Win + R`, type `services.msc`
2. Find **"Windows Update"**
3. Right-click → **Properties**
4. Set **Startup type** to **"Disabled"**
5. Click **"Stop"** if running
6. Click **OK**

---

## ✅ Verify Defender is Disabled

Open PowerShell as Administrator:

```powershell
Get-MpComputerStatus
```

**Expected results:**
- `RealTimeProtectionEnabled: False` ✅
- `AntivirusEnabled: False` ✅
- `AntispywareEnabled: False` ✅
- `IotimeProtectionEnabled: False` ✅

---

## 🚨 Important Notes

> ⚠️ **After Restart**: Check if Defender is still disabled! Windows Updates can re-enable it.

> 💡 **Tip**: Disconnect internet during initial setup to prevent automatic updates.

> 🔄 **If Re-enabled**: Run the disable process again and ensure automatic updates are disabled.

---

## 🛑 Other Antivirus Software

If you have **ANY** other antivirus installed (Norton, McAfee, Avast, AVG, Bitdefender, etc.):

1. **Uninstall completely** from Control Panel
2. **Use their removal tool** (search "[antivirus name] removal tool")
3. **Restart PC**
4. **Verify it's gone**

**You cannot use the spoofer with ANY antivirus running!**

---

**Next Step:** [Download Ethernet Drivers](ethernet-drivers.md) →
