# 🖥️ จอแสดงผลไม่ถูกต้อง (Display Error / UI Glitch)

**CONDITION:** จอดำ, ภาพ UI ไม่เต็มจอ, สัดส่วนเพี้ยน, หน้าต่างโปรแกรมแสดงผิดหน้าจอ (กรณีมีสองจอ)
**OBJECTIVE:** ตั้งค่าความละเอียดภาพ (Resolution) และสัดส่วน (Scaling) ให้กลับมาตรงกับความต้องการของโปรแกรม

## 🚨 IMMEDIATE ACTIONS (Memory Items)
1. **DISPLAY CABLE (HDMI/DP)** ....... **CHECK & RECONNECT**
2. **MONITOR POWER** ................. **CHECK ON**
3. **WINDOWS DISPLAY SETTINGS** ...... **VERIFY RESOLUTION**

## 📋 DIAGNOSTIC CHECKLIST
- [ ] **ขั้นตอนที่ 1: ตรวจสอบการเชื่อมต่อฮาร์ดแวร์จอภาพ**
  - ตรวจสอบว่าสาย HDMI หรือ DisplayPort เสียบแน่นที่การ์ดจอโดยตรง (ไม่เสียบที่เมนบอร์ด หากมีแยก) ลองถอดเสียบใหม่
- [ ] **ขั้นตอนที่ 2: ตั้งค่า Resolution และ Scaling (สำคัญมาก)**
  - คลิกขวาที่ Desktop > `Display Settings`
  - ตรวจสอบ `Display Resolution`: ต้องตั้งเป็น `1920x1080` (หรือตามขนาดตู้ที่กำหนด)
  - ตรวจสอบ `Scale and layout`: ต้องตั้งเป็น `100%` ห้ามเกินกว่านี้ เพราะจะทำให้ UI ของแอปทะลุจอ
- [ ] **ขั้นตอนที่ 3: กรณีใช้สองจอ (Dual Monitor / Kiosk Mode)**
  - เลื่อนจอหลัก (Main Display) ให้ถูกต้องใน Display Settings (ติ๊กถูกที่ `Make this my main display`)
  - ตรวจสอบว่าโปรแกรมถูกลากมาเปิดในจอที่ถูกต้อง หรือใช้คีย์ลัด `Win + Shift + ลูกศรซ้าย/ขวา` ย้ายหน้าต่างโปรแกรม
- [ ] **ขั้นตอนที่ 4: เช็ค Graphics Driver**
  - หากจอมีอาการกะพริบ หรือมีเส้น ให้ลองอัปเดตหรือลงไดร์เวอร์การ์ดจอ (NVIDIA/AMD/Intel) ใหม่แบบ Clean Install

## 🛠️ RESOLUTION & RECOVERY
- บางตู้ใช้หน้าจอแนวตั้ง (Portrait Mode) ตรวจสอบว่า `Display orientation` ถูกตั้งเป็น `Portrait` ตรงกับกายภาพของจอ
