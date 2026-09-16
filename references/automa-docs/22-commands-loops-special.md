# Commands — Loop พิเศษ 2 ตัว (Similar Elements / Excel)

> ที่มา: user สรุปหมวดเฉพาะทางมาให้ (ไม่อยู่ในหมวด Loops โดยตรง)
> วันที่บันทึก: 2026-09-16

## 1. Loop through Similar Elements
- หมวดใน Docs: **Similar Elements** (เมนูซ้าย)
- ใช้วนประมวลผล Element บนเว็บที่โครงสร้างคล้ายกันทั้งหมด
  (เช่น รายการสินค้าหลายชิ้น, ลิสต์ลิงก์บทความ, แถวตารางบนเว็บ)
- วิธีใช้: ระบบหา Selector ของ Element ที่เหมือนกัน แล้ววนอ่านค่า (Text/Attribute) หรือคลิกทีละตัวจนครบ
- ใช้คู่กับ: การจับ Similar Elements (ดูไฟล์ `13-capturing-elements.md`)

## 2. Loop อ่าน Excel (วนทีละแถว/คอลัมน์)
- หมวดใน Docs: **Excel** หรือ **Data Table**
- ใช้อ่านไฟล์ Excel (`.xlsx` / `.csv`) มาวนทีละ Row/Column
- สูตรมาตรฐาน:
  1. เปิด+อ่านไฟล์ (Open Excel / Read Excel)
  2. ส่งข้อมูลเข้า Data Table หรือ List
  3. วนด้วย Loop through Data Table (ดูไฟล์ `19-...`) หรือ For each item in list (ดูไฟล์ `20-...`)
  4. เอาค่าแต่ละแถวไปรัน Process ต่อ
