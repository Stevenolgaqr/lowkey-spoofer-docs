# (INTEL) RAID Reinstallation + Disk Bypass

للأنظمة التي تحتوي على Intel مع دعم RAID.

---

## 🎯 هل تحتاج هذه الطريقة؟

✅ لديك معالج Intel  
✅ لديك قرصين صلبين أو أكثر  
✅ تريد تغيير أعمق للـ Hardware IDs  
✅ مستخدم متقدم

❌ **إذا لديك قرص واحد فقط** → استخدم [Normal Reinstall](normal-reinstall.md)

---

## 📦 المتطلبات

- 💾 قرصين صلبين على الأقل
- 🔧 لوحة أم Intel مع RST
- 💿 Windows ISO  
- 📀 Intel RST Drivers

---

## ⚙️ الخطوة 1: تفعيل RAID في BIOS

```
1. ادخل BIOS (F2 أثناء الإقلاع)
2. اذهب إلى: Advanced > SATA Configuration
3. SATA Mode: RAID
4. احفظ (F10)
```

---

## 🔗 الخطوة 2: إنشاء RAID Volume

**أثناء الإقلاع:**

```
1. اضغط Ctrl + I عند ظهور Intel RAID
2. اختر "Create RAID Volume"
3. املأ:
   • Name: أي اسم
   • RAID Level: 0, 1, 5, أو 10
   • Disks: اختر الأقراص
   • Strip Size: 128KB
4. اضغط Create
```

---

## 💿 الخطوة 3: تثبيت Windows مع RST

### عند تثبيت Windows:

```
1. أقلع من USB
2. عند شاشة الأقراص
3. اضغط "Load Driver"
4. استعرض Intel RST drivers
5. ثبّت Driver
6. سيظهر RAID volume
7. ثبّت Windows
```

**🔗 تحميل Intel RST:**  
[Intel Download Center](https://downloadcenter.intel.com)  
ابحث عن: "Rapid Storage Technology"

---

## 🔢 الخطوة 4: تثبيت RST Software

**بعد Windows:**

```
1. ثبّت Intel RST application
2. افتح البرنامج
3. تحقق من RAID status
4. فعّل write-back cache (اختياري)
```

---

## 🔢 الخطوة 5: Disk Serial Bypass

```cmd
diskpart
list disk
select disk 0
uniqueid disk ID=X9Y8Z7W6
exit
```

> 💡 استخدم Serial عشوائي

---

## ✅ التحقق

افتح Intel RST - يجب أن ترى RAID يعمل بحالة "Normal" ✅

---

**التالي:** [BIOS Configurations](../bios-config.md) →
