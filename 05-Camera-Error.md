# 📷 กล้องไม่ติด (Camera Error)

**CONDITION:** กล้องไม่ทำงาน, ภาพไม่ขึ้นจอภาพ (Black Screen), โปรแกรมแสดงข้อความไม่พบกล้อง (No Camera Found)
**OBJECTIVE:** กู้คืนการเชื่อมต่อกล้องและจับภาพ (Live View) ให้กลับมาทำงานปกติทันที เพื่อไม่ให้กระทบการถ่ายภาพของลูกค้า

## 🚨 IMMEDIATE ACTIONS (Memory Items)
1. **USB CABLE & HUB** ............... **CHECK & RECONNECT**
2. **CAMERA POWER/BATTERY** .......... **CHECK ON & RESTART**
3. **LIVE VIEW BUTTON** .............. **TOGGLE OFF/ON**

## 📋 DIAGNOSTIC CHECKLIST
- [ ] **ขั้นตอนที่ 1: ตรวจสอบ Hardware เบื้องต้น**
  - ตรวจสอบแบตเตอรี่กล้องว่าหมดหรือไม่ (หรือ Dummy Battery เสียบแน่นหรือไม่)
  - สาย USB เชื่อมต่อแน่นทั้งฝั่งกล้องและคอมพิวเตอร์ หรือเสียบผ่าน USB Hub ที่ไฟเลี้ยงพอหรือไม่ (ลองเปลี่ยนไปเสียบตรงที่ Mainboard)
- [ ] **ขั้นตอนที่ 2: รีสตาร์ทกล้อง**
  - ปิดกล้อง (Power OFF) ดึงสาย USB ออก ทิ้งไว้ 10 วินาที
  - เปิดกล้องใหม่ (Power ON) เสียบสาย USB กลับเข้าไป ฟังเสียง Device Connect ของ Windows
- [ ] **ขั้นตอนที่ 3: ตรวจสอบสถานะอุปกรณ์ใน Windows (Device Manager)**
  - คลิกขวา Start > `Device Manager` > ไปที่หมวด `Portable Devices` หรือ `Cameras`
  - ตรวจสอบว่ามีชื่อกล้อง (เช่น Canon EOS, Sony A7) หรือไม่
  - หากมีเครื่องหมายตกใจ (⚠️) ให้คลิกขวา > `Update Driver` หรือ `Disable` แล้ว `Enable` ใหม่
- [ ] **ขั้นตอนที่ 4: ตรวจสอบสถานะโปรแกรมเบื้องหลัง**
  - ตรวจสอบว่าไม่มีโปรแกรมอื่น (เช่น EOS Utility, Sony Imaging Edge) แย่งดึงสัญญาณกล้องไปใช้ หากมีให้ Force Close
- [ ] **ขั้นตอนที่ 5: ตรวจสอบ Log และ Restart Service**
  - รีสตาร์ทโปรแกรมโฟโต้บูธ หากยังไม่ขึ้น ให้ไปดู Log ไฟล์ของระบบ (กด F12 เปิด Console หรือดูไฟล์ Log ในเครื่อง) เพื่อดู error code

## 🛠️ RESOLUTION & RECOVERY
- หากใช้หลายกล้อง ตรวจสอบการตั้งค่า Multi-Camera ในระบบ ว่าเลือก ID กล้องถูกต้อง
- **TIP:** หากมีปัญหาบ่อย ให้เปลี่ยนสาย USB เป็นแบบ Active USB Extension Cable ที่มีคุณภาพ หรือหลีกเลี่ยงการใช้สายที่ยาวเกินไป
