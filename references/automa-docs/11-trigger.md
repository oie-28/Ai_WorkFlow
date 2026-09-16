# Trigger — รัน App อัตโนมัติ (Scheduler / File / Hotkey / Email)

> ที่มา: Features → Main Window → Trigger (Help Center)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: copy-paste จากเว็บ Docs

## ภาพรวม
Trigger ใช้รัน App อัตโนมัติ — กำหนดได้หลายแบบ: ตามเวลา, ไฟล์เปลี่ยน, hotkey, อีเมลเข้า

> ข้อบังคับ: **ต้อง publish App ก่อน** ถึงจะผูก Trigger ได้
> Trigger จะรันเวอร์ชัน **Published ล่าสุด** ไม่ใช่เวอร์ชันที่กำลังแก้ไข

## 1. Scheduler (รันตามเวลา)
- คืออะไร: รัน App ที่กำหนดในเวลาที่กำหนด
- สร้าง: Trigger บนเมนูบน → New → Scheduler
- ตั้งค่า:
  - Name: ชื่อ trigger
  - App: เลือก App ที่ publish แล้ว
  - Frequency: ทุกนาที/ชั่วโมง/วัน/สัปดาห์/เดือน หรือ Advanced ใช้ Crontab expression
  - Queue Execution: ถ้าชนกับ trigger อื่น ให้ต่อคิวแทนที่จะข้าม/บล็อก

## 2. File (รันเมื่อไฟล์เปลี่ยน)
- คืออะไร: รัน App เมื่อไฟล์ที่เฝ้าดูมีการเปลี่ยนแปลง
- สร้าง: Trigger → New → File
- ตั้งค่า:
  - Name / App (publish แล้ว) / Queue Execution (เหมือนข้างบน)
  - Folder: โฟลเดอร์ที่เฝ้าดู + เปิด "Include Subfolders" ได้
  - Event: ชนิด event ที่เฝ้า (เลือกได้หลายอย่าง)
  - File/File type: ชื่อ/นามสกุลไฟล์ เช่น `*.xlsx;*.txt` (คั่นด้วย semicolon **ห้ามเว้นวรรค**)

## 3. Hotkey (รันเมื่อกดปุ่มลัด)
- คืออะไร: รัน App เมื่อกด hotkey ที่ตั้งไว้
- สร้าง: Trigger → New → Hotkey
- ตั้งค่า: Name / App / Hotkey (ปุ่มเสริม Ctrl/Shift/Alt + ปุ่มหลักจาก dropdown) / Queue Execution

## 4. Email (รันเมื่ออีเมลตรงเงื่อนไขเข้า)
- คืออะไร: รัน App เมื่อมีอีเมลเข้าแล้วตรงกฎที่ตั้งไว้
- สร้าง: Trigger → New → Email
- ตั้งค่าทั่วไป:
  - Name / App / Queue Execution (เหมือนข้างบน)
  - Email Server: Gmail / iCloud / custom server
  - Email address: บัญชีที่เฝ้าดู
  - Auth code: รหัสยืนยัน (ดูจาก settings ของอีเมล — **Gmail/iCloud ต้องใช้ app password โดยเฉพาะ ถ้าไม่มีให้ใช้รหัสผ่านอีเมล**)
  - Test connection: กดเทสว่า Automa ต่อเมลได้ไหม (ไม่ได้ให้เช็ค address + auth code)
- Matching Rules (เข้าเงื่อนไขถึงจะทริก):
  - Sender Contains / Recipient Contains / Subject Contains / Body Contains
