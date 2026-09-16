# Commands — Pop-up Handling (5 คำสั่ง)

> ที่มา: Commands → Pop-up Handling (user ถอดเนื้อหามาให้ครบ)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## 1. Upload file(s) — อัปโหลดไฟล์ตรงไม่ผ่าน dialog
- ยิงไฟล์ local ใส่ `<input type="file">` ตรงๆ ไม่ต้องเปิด dialog เลือกไฟล์
- Input: Selector (เช่น `input[type="file"]`) / File Path (absolute path, ใส่หลายไฟล์ได้)
- ตัวอย่าง: Get specified webpage → Upload (`C:\data\report.xlsx`) → Click ปุ่ม Submit

## 2. Download file — โหลดไฟล์ + ตั้งชื่อ/โฟลเดอร์
- Input: File URL หรือ selector ลิงก์โหลด / Save Path-Directory / Rename File (ไม่บังคับ) / Timeout
- Output: full path ไฟล์ที่โหลดลงตัวแปร
- ตัวอย่าง: Download (`https://example.com/file.zip` → `C:\Downloads`) → Wait for file

## 3. Handle download dialog — รับมือ dialog ดาวน์โหลดของ OS/เบราว์เซอร์
- Input: Action (Save/Cancel/Choose save path) / Save Directory-Filename / Timeout (รอ dialog โผล่)
- Output: True/False หรือ path ไฟล์ที่เซฟ
- ตัวอย่าง: Click (ปุ่มที่เรียก download prompt) → Handle (Save → `C:\Downloads\invoice.pdf`)

## 4. Handle upload dialog — รับมือ dialog เลือกไฟล์ของ OS
- Input: File Path เต็ม / Action (Confirm-Open/Cancel) / Timeout (รอ dialog โผล่)
- Output: True/False
- ตัวอย่าง: Click ("Choose File") → Handle (`C:\images\photo.png`, Confirm)

## 5. Handle webpage pop-up dialog — รับมือ JS dialog (Alert/Confirm/Prompt/Permission)
- Input: Dialog Type (Alert/Confirm/Prompt/Permission) / Action (Accept-OK/Dismiss-Cancel/Input text) / Input Text (กรณี Prompt)
- Output: ข้อความใน popup ลงตัวแปร
- ตัวอย่าง: Handle (Accept) → Click (จุดที่เรียก confirm) → Print ข้อความ
- ใช้คู่กับ: Auto handle pop-ups (web) ในไฟล์ `26-commands-webpage.md`
