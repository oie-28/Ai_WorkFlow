# Commands — Data Processing: Datetime + CSV + JSON

> ที่มา: user ถอดเนื้อหามาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## Datetime (7)
1. **Get current datetime** — เวลาปัจจุบัน (Local/UTC) → ตัวแปร (`now_time`)
2. **Add/Subtract datetime** — บวกลบ วัน/เดือน/ปี/ชั่วโมง/นาที (เช่น Subtract 1 Day = เมื่อวาน)
3. **Convert text ↔ datetime** — แปลงตาม Pattern (เช่น `YYYY-MM-DD HH:mm:ss`)
   - ตัวอย่าง: `"2026-09-16"` → คำนวณระยะห่างวัน
4. **Get time interval** — ผลต่าง 2 ช่วงเวลา (Start/End + Unit Days/Hours/Minutes/Seconds)
   - ตัวอย่าง: created_at → now → `diff_days`
5. **Get datetime info** — ดึงส่วนเดียว (Year/Month/Day/Day of week/Hour/Minute/Second)
   - ตัวอย่าง: Day of week → `day_name` → If
6. **Convert datetime → timestamp** — เป็น Unix Epoch (Seconds/Milliseconds)
7. **Convert timestamp → datetime** — กลับเป็น object (เช่น `1773676800` → `dt_object`)
- ใช้กับงานพี่: ประทับเวลาที่ส่งแต่ละชื่อ + ตั้งชื่อไฟล์รายงานรายวัน (ต่อจากไฟล์ 37)

## CSV (2)
8. **Read CSV file** — Path + Delimiter (`,`/`;`) + Encoding (UTF-8/ANSI) + Has Header → Data Table/List
   - ตัวอย่าง: `input.csv` (UTF-8) → `csv_table` → Loop through Data Table
   - ใช้กับงานพี่: รายชื่อรอบใหม่อยู่ใน CSV อ่านตรงได้เลย
9. **Write to CSV file** — Data Table/List → CSV (Path + Overwrite/Append + Delimiter) → path ลงตัวแปร

## JSON (2)
10. **Convert JSON to text** — Object/Dict → string (Compact/Pretty print)
    - ตัวอย่าง: Pretty → `json_str` → HTTP Request
11. **Convert text to JSON** — string → Object/Dict อ่านแยก Key ได้
    - ตัวอย่าง: HTTP Request → `json_obj` → Get value from dictionary
