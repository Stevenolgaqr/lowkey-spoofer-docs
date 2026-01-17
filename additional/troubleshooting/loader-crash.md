# 🔧LOADER CRASH AFTER INSERT LICENSE

Instructions on how to fix loader crash.

***

## Main Cause: Windows Time Not Synchronized

The loader requires accurate system time to verify license.

***

## Solution:

### Step 1: Open Settings

1. Press **Win + I**
2. Go to **Time & Language**
3. Click **Date & Time**

### Step 2: Sync Clock

1. Under **"Synchronize your clock"**
2. Click **"Sync now"** button
3. Wait for synchronization

### Step 3: Restart Loader

1. Close Nova Loader completely
2. Run as Administrator again
3. Enter license key
4. Should work now ✅

***

{% hint style="info" %}
**Still crashing?** Make sure:
* Windows Defender is completely disabled
* No other anti-virus running
* You're running as Administrator
{% endhint %}
