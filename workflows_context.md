# Workflows Context — บริบทงานประจำ

## 1. เครื่องมือหลักที่ใช้
- **Automa** (หลัก): ไฟล์ `line-flow*.automa.json` — โครงสร้าง `drawflow` + `globalData` + `settings`
  - ไฟล์ปัจจุบัน: `line-flow.automa.json`, `line-flow-v7` ถึง `v11`
  - ซอร์สส่วนขยาย: `automa-main/` (business/, src/, utils/, build/)
- **Python**: `floating_note.py` (Tkinter โน้ตลอย), `beeper-center/beeper_center.py`, `beeper-center/beeper_client.py`
- **Beeper / CSV**: `beeper-center/chats.csv`, `accounts.csv`, `config.json`, `requirements.txt`
- **เครื่องมือเสริม (ตามโจทย์):** Make, n8n, Zapier, YAML

## 2. โครงสร้างโปรเจกต์อ้างอิง
```plaintext
1150/
├── Ai_WorkFlow/              # โปรเจกต์นี้ (Agent บริบท + มาตรฐาน)
│   ├── system_prompt.md
│   ├── workflows_context.md  # ไฟล์นี้
│   └── coding_standards.md
├── line-flow*.automa.json    # Workflow Automa หลัก (v7–v11)
├── automa-main/              # ซอร์ส Automa
├── beeper-center/            # สคริปต์ + ดาต้า Beeper
├── floating_note.py          # เครื่องมือโน้ตช่วยงาน
└── opencode-dev/
```

## 3. SOP ประจำ (Standard Operating Procedure)
1. **รับโจทย์:** ระบุเครื่องมือ (Automa / Python / n8n / Make) + input/output ที่คาดหวัง
2. **ออกแบบ Logic:** วาดลำดับ 1-2-3 ก่อนลงบล็อกจริง
3. **ลงมือ:** สร้าง/แก้ JSON (Automa) หรือ Python script
4. **ทดสอบ:** รันจริง 1 รอบ → เก็บ log/error
5. **Debug:** วิเคราะห์ error → แก้เฉพาะจุด → รันซ้ำ
6. **ส่งมอบ:** สรุปขั้นตอน + ไฟล์ + วิธี verify

> กฎ: ถ้าโจทย์ไม่ชัดหรือไม่ระบุเครื่องมือ ให้ถามกลับทันทีก่อนลงมือ
