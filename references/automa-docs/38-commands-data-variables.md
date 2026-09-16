# Commands — Data Processing เพิ่มเติม: Text ขั้นสูง + Variables

> ที่มา: user ถอดเนื้อหามาให้ (ต่อจากไฟล์ `37-commands-data-processing.md`)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## Text ขั้นสูง (4)
1. **Extract from text** — สกัดเฉพาะส่วนด้วย Regex หรือ Prefix/Suffix
   - ตัวอย่าง: Regex `\d{6}` → `otp_code`
2. **Get subtext** — ตัดตาม Start Index (เริ่ม 0) + Length
   - ตัวอย่าง: Start 0 Length 5 → `prefix_id`
3. **Append to text** — ต่อท้ายข้อความเดิม
   - ตัวอย่าง: Append `_processed` → `new_filename`
4. **Pad text** — เติมตัวอักษรให้ครบความยาว (Target Length + Char เช่น `0` + Left/Right)
   - ตัวอย่าง: `42` → `00042` (Length 5, Left)

## Variables & Data Handling (3)
5. **Set variable** — ตั้ง/อัปเดตค่าตัวแปร (ข้อความ/ตัวเลข/Expression)
   - ตัวอย่าง: `status` = Success
6. **Generate random number** — สุ่ม Min-Max (Integer/Decimal) → ตัวแปร
   - ตัวอย่าง: 1–5 → Delay สุ่ม (ใช้หน่วงกันโดนจับบอท)
7. **Acquire asset** — ดึง secret จากที่เก็บปลอดภัยของ Automa (API Key/Password) → ตัวแปร
   - ตัวอย่าง: `SECRET_KEY` → HTTP Request
   - ตรงกับกฎ coding_standards: ห้าม hardcode secret — ใช้ท่านี้แทน
