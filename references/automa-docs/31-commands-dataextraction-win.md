# Commands — Data Extraction (win) (5 คำสั่ง)

> ที่มา: Commands → Data extraction (win) (user ถอดเนื้อหามาให้ครบ)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## 1. Take screenshot of Element (win)
- แคปเฉพาะ Element/ปุ่มบนโปรแกรม → PNG/JPEG + path ลงตัวแปร
- ตัวอย่าง: Focus window → Screenshot Element → Print

## 2. Get Element details (win)
- ดึงลึก: Text / Class Name / AutomationId / Bounding Box → ตัวแปร
- ตัวอย่าง: Detail Text → `win_element_text`

## 3. Get drop-down options text (win)
- ดึง option ทั้งหมดเป็น List
- ตัวอย่าง: Get → `options_list` → For each item in list

## 4. Get window details
- Title / Process Name / PID / Bounds → ตัวแปร
- ตัวอย่าง: Get specified window → Title → `app_title`
- ใช้คู่กับ: Get specified cookie ฝั่งเว็บ (ไฟล์ 28) เวลา debug ข้ามฝั่ง

## 5. Get selected text
- ดึงข้อความที่คลุมไฮไลต์อยู่ (No input) → ตัวแปร
- ตัวอย่าง: Drag mouse คลุม → Get → `selected_str`
