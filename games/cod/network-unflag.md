# Network Unflag - COD

تنظيف الشبكة لـ Call of Duty.

**نفس خطوات EAC/BE!**

---

## 🔧 الخطوات السريعة

### 1. عطّل Adapters الزائدة

`Win + R` → `ncpa.cpl`

عطّل كل شيء إلا Ethernet ✅

---

### 2. ضبط Ethernet

Properties → أطفئ كل شيء إلا IPv4

---

### 3. Advanced Settings

Configure → Advanced:

- Advanced EEE: **Disabled**
- ARP Offload: **Disabled**
- Flow Control: **Disabled**

---

### 4. تنظيف DNS

CMD كـ Admin:
```cmd
ipconfig /flushdns
ipconfig /release
ipconfig /renew
netsh winsock reset
```

أعد التشغيل 🔄

---

### 5. مسح ARP

CMD كـ Admin:
```cmd
arp -d
netsh interface IP delete arpcache
```

أعد التشغيل 🔄

---

✅ **تم!**

**التالي:** [Make New Account](new-account.md) →
