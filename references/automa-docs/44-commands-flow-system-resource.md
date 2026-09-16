# Commands — Flow Control (Subflow) + App & System + Resource Files

> ที่มา: user ถอดเนื้อหาส่วนที่ข้ามมาให้ (ต่อสารบัญให้ครบ)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## Flow Control — Subflow & Function (3)
1. **Run a subflow** — เรียกสคริปต์ย่อย (Subflow Name + Parameters จาก flow หลัก) เสร็จกลับมาทำหลักต่อ
   - ตัวอย่าง: Run (`Login_Process`)
   - ตรงกับหลัก Subflow ใน Core Concepts (ไฟล์ 09): แยกส่วน login/ส่งข้อความ/บันทึกผลเป็น subflow เทสทีละส่วนได้
2. **Call a function** — เรียกฟังก์ชันใช้ซ้ำ (Function Name + Arguments) → Return ลงตัวแปร
   - ตัวอย่าง: Call (`Calc_Tax`, amount) → `tax_val`
3. **Exit this Flow** — หยุด flow ปัจจุบัน (Status Success/Error)
   - ตัวอย่าง: If (ประมวลผลหมดแล้ว) → Exit

## App & System Control (4)
4. **Get trigger failure info** — ดึงรายละเอียดตอน Trigger สั่งแล้วพัง (Trigger Source) → ตัวแปร → Send Mail
5. **Terminate App** — ยุติบอททันที (Force Close ได้) — ใช้ตอน Critical Error ใน Try-Catch
6. **Save custom data** — ฝากค่า Key-Value ข้ามเซสชัน (เช่น Key `last_run` = `now_time`)
7. **Read custom data** — อ่านค่าฝากไว้กลับมา → ตัวแปร
   - ใช้กับงานพี่: จำรอบ/เวลารันล่าสุดข้ามรอบ ไม่ต้องพึ่งไฟล์นอก

## Resource Files (3)
8. **Read resource file** — อ่านไฟล์แนบโปรเจกต์ (Name + Encoding UTF-8) → ตัวแปร
   - ตัวอย่าง: Read (`config.json`) → Convert text to JSON
9. **Get resource file path** — ขอ absolute path ของไฟล์แนบ → ตัวแปร
10. **Copy resource file to folder** — ก๊อปไฟล์แนบออกโฟลเดอร์นอก (Dest เช่น `C:\Reports\`)
