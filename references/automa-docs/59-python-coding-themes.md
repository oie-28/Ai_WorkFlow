# Python & Coding + Themes ใน Automa

> ที่มา: user ถอดเนื้อหามาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## Python Environment & Library (1)
- รัน Python ใน Automa ใช้ lib นอกได้ (Pandas/NumPy/OpenCV/Requests)
- ส่งค่าระหว่าง Flow ↔ Script ผ่าน object `automa`:
  `input_val = automa.get_var("raw_data")` → ประมวลผล → `automa.set_var("clean_data", result)`
- ต่อจาก: Run Python script (ไฟล์ 40) + Execute Python/Shell (ไฟล์ 50)

## Custom Command / Plugin (1)
- สร้าง block เอง (UI Input/Output + โค้ดเบื้องหลัง) จากชุดที่ใช้บ่อย
- ตัวอย่าง: block ต่อ ERP/Database บริษัท → ทีมลากใช้ได้เลย
- ใช้กับงานพี่: ห่อชุด "ค้นหา→คลิก→พิมพ์→ส่ง" เป็น block เดียว reuse ทุกเวอร์ชัน

## Themes & Display (1)
- Light/Dark Mode + ภาษา UI + จัด Layout หน้าต่างทำ flow
- ตัวอย่าง: Dark Mode ลดแสงจ้าตอนทำสคริปต์นานๆ
