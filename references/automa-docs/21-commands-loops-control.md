# Commands — ตัวควบคุม Loop (Next loop / Exit loop / Loop ends)

> ที่มา: Commands → Loops (3 หน้าคำสั่ง)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy เนื้อหา + ถอดตัวอย่างจากรูปมาให้

## 1. Next loop — ข้ามรอบปัจจุบัน ไปรอบถัดไป
> ลิงก์: [Next loop - Automa](https://docs.goautoma.com/rpa/en-US/711601782492966912)
> ข้ามทุกอย่างที่เหลือในรอบนี้ แล้วไปรอบถัดไปทันที
- ใช้ใน: [Loop], [For each item in list], [Loop through Similar Elements (web)]
- Input/Output: ไม่มี
- ตัวอย่าง: Loop 1→10 → If `loop_index` = 5 → Next loop (ข้ามไม่ Print รอบ 5) → Else Print ค่า → วนจนครบ

## 2. Exit loop — ออกจาก loop ทั้งหมด ไปคำสั่งหลัง loop
> ลิงก์: [Exit loop - Automa](https://docs.goautoma.com/rpa/en-US/711600530402258944)
> จบ loop ทันที แล้วรันต่อที่คำสั่งหลัง loop
- ใช้ใน: [Loop], [For each item in list], [For each Similar Elements]
- Input/Output: ไม่มี
- ตัวอย่าง: Loop 1→10 → If `loop_index` = 5 → Exit loop (หยุดเลย รอบ 6–10 ไม่รัน) → Else Print

## 3. Loop ends — จุดปิด loop block
> ลิงก์: [Loop ends - Automa](https://docs.goautoma.com/rpa/en-US/711599584589103104)
> มาร์กจุดจบของ Loop block
- Input/Output: ไม่มี
- ตัวอย่าง: Loop 1→10 step 2 → Print index → Loop ends (จบเมื่อ index เกิน End at)

## สรุปใช้คู่กัน
| ต้องการ | ใช้ตัวไหน |
|---|---|
| ข้ามบางรอบ (เช่น ชื่อนี้ส่งแล้ว ข้ามไป) | If + **Next loop** |
| หยุดทั้ง loop (เช่น ครบโควตา/เจอเงื่อนไขหยุด) | If + **Exit loop** |
| ปิด block (บังคับทุก loop) | **Loop ends** |
