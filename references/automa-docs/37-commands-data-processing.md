# Commands — Data Processing: Text + Number/Date (10 คำสั่ง)

> ที่มา: Commands → Data Processing (user ถอดเนื้อหามาให้ครบ)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## Text (6)
1. **Get length of text** — ความยาวสตริง → ตัวแปร
   > ลิงก์: [Get length of text](https://docs.goautoma.com/rpa/en-US/711435759074918400)
   - ตัวอย่าง: Get → `text_len` → Print
2. **Replace text** — หา+แทนที่ (Regex ได้): Original + Find + Replace with → ตัวแปร
   - ตัวอย่าง: `2025` → `2026` → `updated_str`
3. **Split text** — ตัดด้วย Delimiter (`,`, `\n`) → List
   - ตัวอย่าง: Split (`,`) → `array_list` → For each item in list
4. **Concatenate text** — รวมหลายข้อความเป็นหนึ่ง (+ Separator)
   - ตัวอย่าง: first_name + last_name → `full_name`
5. **Trim text** — ตัดช่องว่างหัวท้าย (Both/Left/Right)
   - ตัวอย่าง: Get Element (web) → Trim → `clean_text`
6. **Change text case** — Uppercase/Lowercase/Title Case
   - ตัวอย่าง: Uppercase → `upper_code`

## Number & Date/Time (4)
7. **Calculate math expression** — สมการ (`(price * qty) * 0.07`) → ตัวแปร
8. **Round number** — ปัดทศนิยม (Round/Floor/Ceil + ตำแหน่ง)
9. **Format date/time** — ฟอร์แมต (`YYYY-MM-DD`, `DD/MM/YYYY hh:mm:ss`) จากปัจจุบัน/ตัวแปร
   - ตัวอย่าง: `YYYYMMDD` → `file_suffix` ตั้งชื่อไฟล์
10. **Add/Subtract date time** — บวกลบวัน/เดือน/ปี/ชั่วโมง (เช่น Add 30 Days → `due_date`)

## สูตรใช้กับงานพี่
Get Element (ชื่อที่อ่านได้) → Trim → (Replace ล้างอักขระกวน) → เทียบกับตารางรายชื่อ
+ Format date/time ทำ `file_suffix` ตั้งชื่อไฟล์ export รายงานส่งแล้วรายวัน
