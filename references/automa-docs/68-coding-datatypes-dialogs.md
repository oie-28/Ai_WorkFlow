# Python Modules + Data Types + Dialogs ขั้นสูง (ทบทวน + ของใหม่)

> ที่มา: user ถอดเนื้อหามาให้ (บางส่วนทบทวนของเดิม + ของใหม่)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## Custom Python (ของใหม่)
1. **Define & Call Custom Functions** — เขียนฟังก์ชันใช้ซ้ำแบบ modular (ในสคริปต์หลักหรือแยกไฟล์ `.py` แล้ว import):
```python
def format_currency(amount):
    return f"฿{amount:,.2f}"

raw_price = automa.get_var("price")
automa.set_var("formatted_price", format_currency(raw_price))
```
2. **Third-Party Management** — pip install (BeautifulSoup/Pandas/Requests) + ห่อ import ใน Try-Except กันรันล่มถ้าไม่มี package
   - ต่อจากไฟล์ `59` / `62`

## Core Data Types (ทบทวน + ตัวอย่างใหม่)
3. **String & Regex** — Trim/Split/Replace/Regex Match/Replace
   - ตัวอย่างใหม่: สกัดอีเมล `\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Z|a-z]{2,}\b`
4. **List & Dictionary** — Push-Append/Filter/Sort/Merge/Get Key
   - ตัวอย่าง: Extract Table → List (กรองตามเงื่อนไข) → Save Variable

## Mouse/Visual, Data Table, Excel, Desktop/SAP (ทบทวน — ดูไฟล์ละเอียด)
5. **Mouse & Keyboard / Visual** — Type/Click/Move/Scroll + Click-Move to Image (Accuracy 80–95%) + Human Simulation (Bezier)
   → รายละเอียดไฟล์ `33`
6. **Data Table Ops** — Read/Write/Clear/Count + Row/Column control + Import-Export (CSV/JSON)
   → รายละเอียดไฟล์ `34`
7. **Excel Advanced (ของใหม่)** — Run Macro (VBA) / Set Cell Format / Create-Refresh PivotTable / Export PDF +
   Get first free row-column / **Delete duplicated rows** (ลบแถวซ้ำอัตโนมัติ — ใช้กันรายชื่อซ้ำได้อีกทาง)
   → พื้นฐานไฟล์ `35`–`36`
8. **Desktop & SAP (ทบทวน)** → รายละเอียดไฟล์ `30` / `32`

## Dialogs ขั้นสูง (ของใหม่)
9. **User Input & Confirm** — confirm dialog (True/False) / input dialog / **select file-folder dialog** (ให้ user เลือกไฟล์/โฟลเดอร์จากเครื่อง)
10. **Custom Form & Notification** — notification มุมจอ / **Data Table dialog** (โชว์ตารางให้ตรวจก่อนกดยืนยัน) / custom dialog หลายช่อง
    - ใช้กับงานพี่: โชว์ตารางรายชื่อรอบนั้นให้ตรวจก่อนกดยืนยันส่ง (กันส่งผิดล็อต)
