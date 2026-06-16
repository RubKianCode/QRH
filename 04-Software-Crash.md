# 💥 โปรแกรมค้างหรือปิดเอง (Software Crash / Freeze)

**CONDITION:** โปรแกรมหยุดทำงานกะทันหัน, หน้าจอสัมผัสไม่ตอบสนอง (UI Freeze), หรือโปรแกรมปิดตัวเองเด้งออกไปหน้า Desktop
**OBJECTIVE:** ปิดกระบวนการที่ค้างอย่างปลอดภัย ป้องกันไฟล์และฐานข้อมูลเสียหาย และกู้คืนระบบให้พร้อมถ่ายเร็วที่สุด

## 🚨 IMMEDIATE ACTIONS (Memory Items)
1. **TOUCH INPUT** ................... **CEASE IMMEDIATELY**
2. **SYSTEM REBOOT** ................. **DO NOT FORCE REBOOT YET**
3. **PROCESS MANAGER** ............... **FORCE CLOSE (END TASK)**

## 📋 DIAGNOSTIC CHECKLIST
- [ ] **ขั้นตอนที่ 1: Force Close ผ่าน Task Manager**
  - กด `Ctrl + Shift + Esc` (หรือ Ctrl+Alt+Del) เพื่อเปิด Task Manager
  - ค้นหาโปรแกรมโฟโต้บูธ (รวมถึงกระบวนการย่อยของ Electron) คลิกขวา > `End Task`
- [ ] **ขั้นตอนที่ 2: ตรวจสอบทรัพยากรระบบ (System Resource Check)**
  - **RAM:** ไปที่แท็บ `Performance` > `Memory` หาก RAM ขึ้น 95-100% แสดงว่าเกิด Memory Leak
  - **Disk Space:** ตรวจสอบ Drive C: และ Drive เก็บรูปภาพ ควรมีพื้นที่ว่างเหลืออย่างน้อย 5GB-10GB เสมอ หากเต็มให้เคลียร์ไฟล์ Temp หรือรูปภาพเก่า
- [ ] **ขั้นตอนที่ 3: ตรวจสอบ Windows Event Viewer (หาต้นตอ)**
  - ค้นหา `Event Viewer` ในช่อง Start > เปิดไปที่ `Windows Logs` > `Application`
  - มองหาสัญลักษณ์กากบาทสีแดง (Error) ในเวลาที่โปรแกรมดับ เพื่อดูว่า Module ไหนทำงานผิดพลาด (เช่น ntdll.dll, GPU driver)
- [ ] **ขั้นตอนที่ 4: ตรวจสอบและเคลียร์ Temp Files / Cache**
  - กด `Win + R` พิมพ์ `%temp%` และลบไฟล์ชั่วคราวทั้งหมด
  - เคลียร์ Cache ของแอปพลิเคชันในโฟลเดอร์ AppData ถ้าจำเป็น
- [ ] **ขั้นตอนที่ 5: Restart Service & App**
  - เปิดโปรแกรมใหม่ สังเกตหน้า Loading Screen ว่ามี Error แจ้งเตือนหรือไม่

## 🛠️ RESOLUTION & RECOVERY
- หากเกิดจากการพิมพ์รูปพร้อมกันจำนวนมาก ให้ตั้งคิวกระดาษ (Print Queue) ให้ทยอยพิมพ์
- **WARNING:** หากค้างบ่อยๆ อาจต้องเช็คความร้อนของคอมพิวเตอร์ (CPU/GPU Temperature) หรืออัปเดตเวอร์ชันของโปรแกรมล่าสุด
