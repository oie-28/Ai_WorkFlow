# Commands — Browser & File & Scraping (ชุดพื้นฐานรวม)

> ที่มา: user ถอดเนื้อหาส่วนที่ข้ามมาให้ (ต่อสารบัญให้ครบ)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้
> หมายเหตุ: บางตัวซ้ำกับไฟล์ละเอียดที่มีแล้ว (25/26/24) — ไฟล์นี้เก็บมุมมองสูตรรวม

## Browser Interactivity พื้นฐาน (3)
1. **Click Element** — คลิกตาม Selector (Single/Double/Right)
2. **Type Text / Fill Field** — กรอกช่อง (Selector + Text + Clear Field First)
3. **Take Screenshot** — Full Page/Element → path/base64 (ต่อ Automa AI ได้)

## System & Screen Control (2)
4. **Enable/Disable screen saver** — ปิดตอนรันงานยาว (Disable → Run Long Task → Enable)
5. **Set/Clear screen saver message** — ข้อความโชว์ตอนพักจอ (เช่น "Automa is running...")
   - ใช้กับงานพี่: กันจอล็อก/พักตอน loop ส่งยาวๆ

## Browser Advanced — Tab & Window (3)
6. **Open/Switch/Close tab** — New tab (+URL) / Switch (Index/Title) / Close → tab ID ลงตัวแปร
7. **Navigation** — Go to URL / Reload / Back / Forward
8. **Handle Alert/Dialog** — Accept/Dismiss/Prompt Text

## File & Folder Operations (3)
9. **Create/Delete Directory** — สร้าง/ลบโฟลเดอร์ (เช่น `C:\Automa_Logs\` → เขียน CSV ลงไป)
10. **Move/Copy/Rename File** — ย้าย/ก๊อป/เปลี่ยนชื่อ (เช่น Downloads → Processed — แยกไฟล์รายชื่อที่ส่งแล้ว)
11. **Check File Exists** — มีไฟล์ไหม → true/false → If
    - ใช้กับงานพี่: เช็คไฟล์รายชื่อรอบใหม่มาก่อนรัน

## Web Scraping & Element Extraction (2)
12. **Get Element Text/Attribute** — Text หรือ href/src/value → ตัวแปร (เช่น → `price` → คำนวณต่อ)
13. **Get Similar Elements (Extract List)** — ดึงชุดที่ซ้ำกัน → List/Data Table
    - ตัวอย่าง: Get → `products_list` → Write to CSV file
