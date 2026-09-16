# Commands — Data Processing: List + Dictionary

> ที่มา: user ถอดเนื้อหามาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## List (6)
1. **Create new list** — สร้าง List ว่าง (List Name)
   - ตัวอย่าง: Create (`user_emails`) → Loop → Add item
2. **Add item to list** — เพิ่มข้อมูล (Target List + Item Value + Position: At the end / At specified index)
   - ตัวอย่าง: Extract data → Add (`extracted_val`)
3. **Get item at specified index** — ดึงตาม Index (เริ่ม `0`, `-1` = ตัวสุดท้าย) → ตัวแปร
4. **Get length of list** — นับจำนวน → ตัวเลข
   - ตัวอย่าง: Get → `total_items` → If (> 0 ไหม)
5. **Sort list** — Ascending / Descending → For each ต่อ
6. **Remove duplicate items** — เหลือเฉพาะ unique
   - ตัวอย่าง: Get Similar Elements → Remove dup → Export Data Table
   - ใช้กับงานพี่: กันรายชื่อซ้ำก่อนวนส่ง

## Dictionary (6)
1. **Create new dictionary** — สร้าง dict ว่าง (เช่น `user_profile`)
2. **Set key-value pair** — เพิ่ม/อัปเดต (Target + Key + Value เช่น status = Active)
3. **Get value from dictionary** — อ่านตาม Key → ตัวแปร
   - ตัวอย่าง: Key `token` → `auth_token` → HTTP Request
4. **Get list of keys** — Key ทั้งหมด → List (เช่น `user_info` → `keys_list` → For each)
5. **Get list of values** — Value ทั้งหมด → List
6. **Remove key-value pair** — ลบคู่ Key-Value (เช่น ลบ `temp_token` หลังใช้เสร็จ — ดีต่อความปลอดภัย)
