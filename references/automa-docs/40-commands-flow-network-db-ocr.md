# Commands — Flow Control + Network + Database + OCR/Scripting

> ที่มา: user ถอดเนื้อหามาให้ (หมวด Loop/Flow Control, Network & HTTP, Database, OCR & Scripting)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## Loop & Flow Control (4)
1. **Loop** — 3 โหมด: Times (จำนวนรอบ) / Condition (จนเงื่อนไขจริง) / Element-List (ตามรายการ); เก็บ index (เริ่ม 0)
   - ตัวอย่าง: Times 10 → Click → Loop Ends
2. **If condition** — Branch True/False (Variable + Operator Equals/Contains/Greater Than/Is Empty + Compare Value)
   - ตัวอย่าง: status == Success → True: Export Log / False: Display Notification
3. **Delay / Wait** — หน่วงวินาที/มิลลิวินาที/นาที (สุ่ม Min-Max ได้)
   - ตัวอย่าง: Click → Delay 3–5s → Get Text
4. **Try-Catch** — ดัก error กันบอทหยุดกลางคัน (Error Action / Skip to next step + เก็บ error message ลงตัวแปร)
   - ตัวอย่าง: Try Click → Catch (หาปุ่มไม่เจอ) → Refresh Page

## Network & HTTP (3)
5. **HTTP Request** — GET/POST/PUT/DELETE (URL + Headers/Body JSON) → Response + Status ลงตัวแปร
   - ตัวอย่าง: POST → `api_res`
6. **Send Mail** — SMTP (Host/Port/User/Pass) + ผู้รับ/หัวข้อ/Body/แนบไฟล์
   - ตัวอย่าง: Export Data Table → Send Mail (แนบ report.xlsx) — ใช้ส่งรายงานส่งแล้วรายวันได้
7. **FTP Operations** — Upload/Download/Delete (Host/Port/Credentials + Local/Remote Path)

## Database (3)
8. **Connect to database** — MySQL/PostgreSQL/SQL Server/SQLite (Type + Connection String) → handle (`db_conn`)
9. **Execute SQL statement** — SELECT/INSERT/UPDATE/DELETE → ผลลง List/Data Table
10. **Batch insert to database** — Bulk จาก Data Table → ตารางปลายทาง (เช่น logs)

## OCR & Scripting (2)
11. **General OCR** — รูป/Screenshot/PDF → ข้อความ (เลือกภาษา English/Thai)
    - ตัวอย่าง: Screenshot → OCR → `extracted_txt`
12. **Run Python script** — โค้ด/ไฟล์ `.py` + Arguments → Return ลงตัวแปร
    - ใช้ตอนคำนวณซับซ้อนที่ block ธรรมดาทำไม่ได้

## สูตรใช้กับงานพี่
- Try-Catch ครอบขั้นคลิก Chat/Friends (จุดพังบ่อย) → Catch: Refresh + ลองใหม่ ไม่ให้ loop ล่มทั้งล็อต
- Send Mail แนบรายงาน + Display notification สรุปผลท้ายงาน
- Run Python สำหรับล้างรายชื่อซับซ้อนก่อนเทียบตาราง
