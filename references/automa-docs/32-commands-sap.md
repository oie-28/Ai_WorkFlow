# Commands — SAP (10 คำสั่ง)

> ที่มา: Commands → SAP (user ถอดเนื้อหามาให้ครบ)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้
> หมายเหตุ: หมวดเฉพาะทาง — งานปัจจุบันของโปรเจกต์ยังไม่ใช้ SAP เก็บไว้อ้างอิง

## สูตรมาตรฐาน SAP
Execute transaction (T-Code) → Wait for SAP to load → อ่าน/สั่งงาน → เช็ค Status bar

## รายคำสั่ง
1. **Select tree node** — คลิก node ใน tree (Node Path เช่น `\Finance\General Ledger\Accounts`)
2. **Click Toolbar Button** — กดปุ่ม toolbar (Button ID/Name เช่น Save/Back/Execute)
3. **Count rows in table** — นับแถว → ตัวแปร (เช่น `total_rows` → Loop)
4. **Count columns in table** — นับคอลัมน์ → ตัวแปร
5. **Wait for SAP to load** — รอประมวลผลเสร็จ + timeout → True/False
6. **Execute transaction** — รัน T-Code ตรง (เช่น `VA01`, `SE16N`, `ME21N`)
7. **Get status bar info** — อ่าน Message Text/Type (Success/Error/Warning) → If เช็ค error
8. **Select menu item** — เมนูบน (Menu Path เช่น `List > Export > Local File`)
9. **Select date** — วันที่ (Date Value เช่น `2026-09-16` หรือตัวแปร)
10. **Read table content** — อ่านตารางทั้งก้อน → Data Table (All rows/ช่วง) → Export ต่อ
