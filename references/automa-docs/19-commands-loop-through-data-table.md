# Commands — Loop through Data Table

> ที่มา: [Loop through Data Table - Automa](https://docs.goautoma.com/rpa/en-US/716545844522442752)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy เนื้อหา + ถอดตัวอย่างจากรูปมาให้

## คำอธิบาย
วนเนื้อหาใน Data Table แล้วเก็บ item ที่วนไว้ใช้

## พารามิเตอร์
- **Loop through** — ขอบเขตที่จะวน:
  - **Row:** วนทีละแถว แต่ละแถวกลายเป็น list 1 มิติ
  - **Column:** วนทีละคอลัมน์ แต่ละคอลัมน์กลายเป็น list 1 มิติ
  - **Range:** วนทีละแถวในช่วงที่ระบุ
  - **Used Range:** วนทีละแถวเฉพาะบริเวณที่มีข้อมูล
- **Row number** — แถวเริ่มต้น (นับจาก `1`, ใส่ลบได้ เช่น `-1` = แถวสุดท้าย)
- **Column number** — คอลัมน์เริ่มต้น (นับจาก `1`, ใส่ลบได้ เช่น `-1` = คอลัมน์สุดท้าย)
- **Save each item to** — เก็บ item/ค่าของรอบปัจจุบันลงตัวแปร
- **Save each row number to** — เก็บเลขแถวของรอบปัจจุบันลงตัวแปร

## ตัวอย่าง (ถอดจากรูปใน Docs)
Flow: `[Loop through Data Table]` วน used range → `[Print]` ค่าแต่ละรอบ → `[Loop ends]`

**ข้อมูลใน Data Table (5 แถว × 5 คอลัมน์ A–E):**

| Row | A | B | C | D | E |
|---|---|---|---|---|---|
| 1 | 2 | 6 | 7 | 2 | 7 |
| 2 | 9 | 3 | 4 | 9 | 3 |
| 3 | 1 | 4 | 9 | 5 | 2 |
| 4 | 5 | 7 | 2 | 6 | 1 |
| 5 | 9 | 3 | 7 | 5 | 2 |

**Flow Steps:**
- Step 1: `Loop through Data Table` — วนเนื้อหาทั้งหมด เก็บแต่ละรอบลง `loop_datatable` + เลขแถวลง `loop_item_rownum`
- Step 2: `Print` — พิมพ์ `[Information]` `loop_datatable`
- Step 3: `Loop ends` — ปิด loop

**Execution Logs (หลักฐานว่าแต่ละรอบได้ list 1 แถว):**

| Type | Time | Content | Process | Line |
|---|---|---|---|---|
| Info | 2025-04-18 11:31:42.299 | Execution started... | | |
| Info | 2025-04-18 11:31:42.406 | [2, 6, 7, 2, 7] | Main Flow | 2 |
| Info | 2025-04-18 11:31:42.407 | [9, 3, 4, 9, 3] | Main Flow | 2 |
| Info | 2025-04-18 11:31:42.407 | [1, 4, 9, 5, 2] | Main Flow | 2 |
| Info | 2025-04-18 11:31:42.408 | [5, 7, 2, 6, 1] | Main Flow | 2 |
| Info | 2025-04-18 11:31:42.433 | [9, 3, 7, 5, 2] | Main Flow | 2 |
| Info | 2025-04-18 11:31:42.433 | Execution ended | | |
