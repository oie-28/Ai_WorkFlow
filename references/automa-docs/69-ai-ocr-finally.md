# AI & OCR + Try-Catch-Finally (ส่วนใหม่)

> ที่มา: user ถอดเนื้อหามาให้ (ส่วน Mouse/DataTable/Excel/Desktop/SAP ที่ส่งมาด้วยซ้ำกับไฟล์เดิม — ดูไฟล์ `33`/`34`/`35`/`30`/`32`)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## AI & OCR Nodes (ใหม่)
1. **Automa AI (LLM)** — Prompt (ฝังตัวแปรได้) + เลือกโมเดล/ปรับ Temperature/Max Tokens → ผลลัพธ์ลงตัวแปร
   - ตัวอย่าง: Extract → AI วิเคราะห์ Sentiment รีวิว → If
   - ต่อจากไฟล์ `43` (รอบนี้ได้รายละเอียดพารามิเตอร์เพิ่ม)
2. **General & Table OCR** — General (ภาพ→String) / **General + position** (ข้อความพร้อมพิกัด X-Y) / **Table OCR** (รูปตาราง→Data Table)
   - ตัวอย่าง: Screenshot → Table OCR → Write to Data Table → Export Excel
   - ใช้กับงานพี่: รายชื่ออยู่ในรูป/สแกนดึงด้วย Table OCR ได้

## Try - Catch - Finally (ใหม่: มี Finally)
- **Try:** งานหลัก / **Catch:** ทางสำรองตอน error (เช่น ส่ง LINE + แคปจอ) / **Finally:** ทำเสมอไม่ว่าพังหรือไม่ (เช่น ปิดเบราว์เซอร์/Excel/Disconnect DB)
- สูตร: Try (รันหลัก) → Catch (ภาพ error → Telegram) → Finally (ปิดเบราว์เซอร์)
- ต่อจากไฟล์ `40` (เดิมมีแค่ Try-Catch) — แนะนำให้ Finally ปิดแท็บ/เซฟตารางทุกครั้ง กันของค้าง

## Resource Files (ทบทวน — ดูไฟล์ `44`)
- Read / Copy to folder (เช่น ดึง Template ใบเสร็จมาสร้างเอกสารใหม่)
