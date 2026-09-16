# Commands — Data Table (10 คำสั่ง)

> ที่มา: Commands → Data Table (user ถอดเนื้อหามาให้ครบ)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## อ่าน/เขียน
1. **Read Data Table** — อ่านทั้งก้อน (All rows) / แถวเดียว / ช่วงแถว + Column Filter → List/Object ลงตัวแปร
   - ตัวอย่าง: Read All → `table_data` → For each item in list
2. **Write to Data Table** — Append row (ต่อท้าย) / Update cell (แก้เฉพาะช่อง: Row Data-Value + Target Column-Row Index)
   - ตัวอย่าง: Extract data → Write (Append `[row_data]`)
3. **Count rows in Data Table** — นับแถว → ตัวเลข
   - ตัวอย่าง: Count → `total_rows` → Loop (0 ถึง total_rows)
4. **Delete row from Data Table** — ลบตาม Row Index (เริ่ม `0`)
5. **Delete column from Data Table** — ลบตามชื่อ/ดัชนีคอลัมน์
6. **Clear Data Table** — ล้างทั้งตาราง (แล้ว Extract ชุดใหม่ทับได้)

## เข้า/ออกไฟล์
7. **Import to Data Table** — CSV/Excel → ตาราง (File Path + Format + Has Header)
   - ตัวอย่าง: Import (`input.csv`) → Loop through Data Table
8. **Export Data Table** — ตาราง → CSV/Excel/JSON (+ path ลงตัวแปร)
   - ตัวอย่าง: Extract → ตาราง → Export (`C:\reports\out.xlsx`)

## คำอธิบายคอลัมน์
9. **Get column description** — อ่านคำอธิบายคอลัมน์ → ตัวแปร
10. **Set column description** — ใส่คำอธิบาย (เช่น Status = "Process result state")

## สูตรมาตรฐาน
Import (CSV/Excel) → Loop through Data Table → ประมวลผล → Export (Excel/JSON) เก็บหลักฐาน
