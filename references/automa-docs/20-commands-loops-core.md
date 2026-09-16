# Commands — Loops หลัก 5 ตัว (Loop / While / For each list / For each dict / Infinite)

> ที่มา: Commands → Loops (5 หน้าคำสั่ง)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy เนื้อหา + ถอดตัวอย่างจากรูปมาให้

## 1. Loop — วน N รอบตายตัว
> ลิงก์: [Loop - Automa](https://docs.goautoma.com/rpa/en-US/711607566972981248)
> วน block คำสั่งตามจำนวนที่กำหนด
- **Start from** — index เริ่มต้น
- **End at** — index สิ้นสุด (ถึงแล้วจบ loop)
- **Increment by** — ค่าเพิ่มต่อรอบ
- **Save each value to** — เก็บค่า index รอบปัจจุบัน (เช่น `loop_index`)
- ตัวอย่างจากรูป: Start `1` → End `10` → Increment `2` → Print ค่าทีละรอบจนจบ

## 2. While loop — วนจนกว่าเงื่อนไขจะไม่จริง
> ลิงก์: [While loop - Automa](https://docs.goautoma.com/rpa/en-US/711606318642102272)
> วน block จนกว่า condition จะไม่เป็น True
- Operand 1: ปิด Python mode กรอกข้อความ / เปิด Python mode กรอก expression / จิ้มตัวแปร
- Operator: เช่น Greater than / Contains / Starts with
- Operand 2: ตั้งแบบเดียวกับ 1 (operator operand เดียว เช่น Is True / Is empty ช่อง 2 ถูกข้าม)
- Output: ไม่มี
- ตัวอย่างจากรูป: Operand 1 = `variable`, Operator = `Less than`, Operand 2 = `50`
- ตัวอย่าง flow: ตั้ง int = 10 → While < 50 → Print ค่า + บวกทีละ 10 → วนจนเงื่อนไขเท็จ

## 3. For each item in list — วนทีละตัวใน list
> ลิงก์: [For each item in list - Automa](https://docs.goautoma.com/rpa/en-US/711605038084767744)
> วน item ใน list ทีละตัว
- **List:** กรอก list หรือเลือกจากคำสั่งก่อนหน้า เช่น `['United States', 'Germany', 'Japan']`
- **Output loop index:** ติ๊ก = ได้ index ของแต่ละรอบด้วย
- **Save each item to:** เก็บ item รอบปัจจุบัน (เช่น `loop_item`)
- **Save each loop index to:** เก็บ index รอบปัจจุบัน (เช่น `loop_item_index`, ต้องติ๊กข้อบนก่อน)
- หมายเหตุ: ฟอร์แมต `list = [value1, value2, value3]` ใส่ได้ทุกชนิด — **index เริ่มที่ 0**
- **Start from:** index เริ่ม (default `0` = ต้น list)
- **End at:** index หยุด (default `-1` = ท้าย list)
- ตัวอย่างจากรูป: List 3 ประเทศ + ติ๊ก Output loop index → เก็บ `loop_item` + `loop_item_index`
- ตัวอย่าง flow: วน list → Print item + index ทีละรอบจนตัวสุดท้าย

## 4. For each key-value pair in dictionary — วนทีละคู่ใน dict
> ลิงก์: [For each key-value pair in dictionary - Automa](https://docs.goautoma.com/rpa/en-US/711604147847938048)
> วนทีละ key-value ใน dictionary
- **Dictionary:** เลือก object จากคำสั่งก่อนหน้า หรือกรอกเอง เช่น `{"name":"Automa","location":"New York, United States"}`
- **Save each key to:** เก็บ key รอบปัจจุบัน (เช่น `loop_key`)
- **Save each value to:** เก็บ value รอบปัจจุบัน (เช่น `loop_value`)
- หมายเหตุ: ฟอร์แมต `dict = {key1: value1, key2: value2}` — value เป็นชนิดใดก็ได้
- ตัวอย่าง flow: วน dict → Print key + value ทีละคู่จนคู่สุดท้าย

## 5. Infinite loop — วนไม่รู้จบ (ออกด้วยเงื่อนไขข้างใน)
> ลิงก์: [Infinite loop - Automa](https://docs.goautoma.com/rpa/en-US/711603091046633472)
> วนไม่สิ้นสุด — ไม่มี input
- Output: เก็บ index รอบปัจจุบันได้ (เช่น `loop_index`)
- ตัวอย่าง flow: `[Get specified webpage]` → Infinite loop → `[If webpage contains]` เช็ค element โผล่ไหม → วนต่อจนกว่าเงื่อนไขจะตรง (element ปรากฏ)

## หมายเหตุ (จาก Core Concepts ไฟล์ 09 — ใช้ประกอบ)
- ทุก loop block ต้องมี `[Loop ends]` ปิด ไม่งั้น error
- ออกก่อนครบ: `[Exit loop]` / ข้ามรอบปัจจุบัน: `[Next loop]`
- Loop อีก 2 แบบที่เหลือ (ยังไม่บันทึก): Loop through Similar Elements, Loop through Excel worksheet content
