# Coding Standards & Guidelines

## 1. Automa JSON (`*.automa.json`)
- เก็บโครงหลัก: `name`, `description`, `drawflow`, `globalData`, `settings`, `table`
- ตั้งชื่อ workflow: `kebab-case` + เวอร์ชัน เช่น `line-flow-v12`
- ห้าม hardcode ค่าลับใน `globalData` — ใช้ variable / vault แทน
- ก่อนส่งมอบ: export JSON แล้ว validate ว่า import กลับได้

## 2. Python
- Python 3.x, `utf-8` ทุกไฟล์, ใช้ `pathlib` จัดการ path
- ตั้งชื่อ: ไฟล์ `snake_case.py`, ฟังก์ชัน `snake_case`, คลาส `PascalCase`, ค่าคงที่ `UPPER_SNAKE`
- Error handling มาตรฐาน:
```python
try:
    main()
except Exception as e:
    print(f"[ERROR] {e}")
    raise
```
- สคริปต์ช่วยงาน (เช่น `floating_note.py`) ต้องรันเดี่ยวได้ ไม่พึ่งพา path เฉพาะเครื่อง

## 3. YAML / Config / CSV
- YAML: indent 2 spaces, key เป็น `snake_case`
- CSV (`chats.csv`, `accounts.csv`): แถวแรกต้องเป็น header, encoding `utf-8-sig`
- `config.json`: แยกค่าลับออก — ใช้ env var หรือไฟล์ `.env` ที่ไม่ commit

## 4. ความปลอดภัย
- ห้ามวาง `API Key`, `Password`, `Token` ในโค้ด/JSON ที่ส่งมอบ
- ใช้ placeholder เช่น `{{API_KEY}}`, `os.getenv("BEEPER_TOKEN")`
- ตัวอย่าง secret ให้ใช้ `secrets.blank.js` เป็นต้นแบบ

## 5. รูปแบบการส่งมอบ
ทุกครั้งต้องมี 4 ส่วน:
1. Overview Logic
2. Step-by-Step Execution Plan
3. Code Snippet / Config
4. Verification Step
