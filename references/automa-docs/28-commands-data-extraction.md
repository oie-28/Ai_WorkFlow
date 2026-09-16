# Commands — Data Extraction (12 คำสั่งดึงข้อมูล)

> ที่มา: Commands → Data Extraction (user ถอดเนื้อหามาให้ครบ)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## 1. Extract data — ขูดข้อมูลมีโครงสร้าง
- ดึง Text/Link/Image URL/Attribute จาก element เดี่ยวหรือหลายตัวพร้อมกัน → Data Table หรือตัวแปร
- Input: Selector / Extraction Columns (Text, Link href, Image src, Attribute) / Save to (Data Table-Variable)
- Output: ชุดข้อมูล List/JSON
- ตัวอย่าง: Get specified webpage → Extract (`.product-card` → Data Table)

## 2. Take screenshot of webpage — แคปจอ
- Scope: Visible area / Full page / Element (+ Selector) → PNG-JPEG หรือ Base64 ลงตัวแปร
- ตัวอย่าง: Navigate → Wait loaded → Screenshot (Full page)

## 3. Get Element details (web) — รายละเอียด element ตัวเดียว
- Detail Type: Text / HTML-OuterHTML / Tag Name / Class Name / Bounding Box / Attribute
- ตัวอย่าง: `#submit-btn` Class Name → `btn_class`

## 4. Get drop-down options text (web) — รายชื่อ option ทั้งหมด
- Get Type: Option Text / Option Value → List
- ตัวอย่าง: `#country-select` → `country_list` → For each

## 5. Get webpage details — ข้อมูลระดับเพจ
- Property: Title / URL / Page Source / Cookies string / User Agent
- ตัวอย่าง: URL → `current_url` → If เช็คเงื่อนไข

## 6. Get scrollbar position — ตำแหน่ง scroll
- Scope: Page/Element + Axis Y-X → พิกเซลลงตัวแปร
- ตัวอย่าง: Y → `y_pos` → If เช็คว่าเลื่อนถึงจุดหรือยัง

## 7. Get webpage dialog content — ข้อความใน popup
- Dialog Type: Alert/Confirm/Prompt → ข้อความลงตัวแปร
- ตัวอย่าง: Auto handle pop-ups → Get dialog → `dialog_msg` → Print

## 8. Get list of cookies — คุกกี้ทั้งหมด
- Domain Scope: ปัจจุบัน/ระบุมา → array cookie
- ตัวอย่าง: Get → `all_cookies` → ดึง Session/Token ต่อ

## 9. Get specified cookie — คุกกี้ตัวเดียว
- Cookie Name (เช่น `session_id`, `auth_token`) + Domain → Value/object
- ตัวอย่าง: `session_token` → `token`

## 10–12. Network monitoring (3 คำสั่งใช้เป็นชุด)
- **Start monitoring web requests** — เปิดดัก HTTP/HTTPS: URL Filter (เช่น `*api/v1/*`) + Resource Type (XHR-Fetch/Image/Script/Document)
- **Stop monitoring web requests** — หยุดดัก (No input/output)
- **Get monitoring results** — ดึง log (URL/Headers/Body/Status/Response) แบบ JSON List หรือ Raw → ตัวแปร
- ตัวอย่างชุด: Start (filter `*api/data*`) → Click (ปุ่มเรียก API) → Stop → Get → `network_logs` → Run JavaScript แกะ JSON
