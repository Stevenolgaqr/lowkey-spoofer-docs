# 3️⃣Disable Windows Defender

{% hint style="danger" %}
**CRITICAL:** Windows Defender MUST be completely disabled for spoofer to work!
{% endhint %}

***

## Method 1: Manual Disable (Recommended)

1. Press **Win + I** to open Settings
2. Go to **Update & Security**
3. Click **Windows Security**
4. Click **Virus & threat protection**
5. Click **Manage settings**
6. Turn **OFF** all options:
   * Real-time protection
   * Cloud-delivered protection
   * Automatic sample submission
   * Tamper Protection

***

## Method 2: Using dControl (Most Effective)

{% file src="../.gitbook/assets/dControl.zip" %}
dControl - Windows Defender Disabler
{% endfile %}

1. Download dControl from link above
2. Extract the ZIP file
3. Run **dControl.exe** as Administrator
4. Click **Disable Windows Defender**
5. Restart PC
6. Verify Defender is disabled

***

## Method 3: Registry Edit

{% hint style="warning" %}
Advanced users only!
{% endhint %}

```batch
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows Defender" /v DisableAntiSpyware /t REG_DWORD /d 1 /f
```

***

## Method 4: Batch Script

Create a `.bat` file with this content and run as Admin:

```batch
@echo off
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows Defender" /v DisableAntiSpyware /t REG_DWORD /d 1 /f
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows Defender\Real-Time Protection" /v DisableRealtimeMonitoring /t REG_DWORD /d 1 /f
pause
```

***

{% hint style="success" %}
**Verification:** Check Windows Security - it should show "No active antivirus provider"
{% endhint %}
