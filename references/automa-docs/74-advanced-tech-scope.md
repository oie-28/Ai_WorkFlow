# เทคนิคขั้นสูง — Shadow DOM + Multi-tab + Variable Scope (ของใหม่)

> ที่มา: user ถอดเนื้อหามาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## 1. Shadow DOM & iFrame (โค้ดพร้อมใช้)
- สลับ Context เข้า iFrame ก่อน หรือเจาะ shadowRoot ด้วย JS:
  `document.querySelector('...').shadowRoot.querySelector('...')`
- ต่อจาก FAQ ไฟล์ `62` (รอบนี้ได้ snippet ตรง)

## 2. Multi-Tab Aggregation
- สูตร: Switch Tab / Navigate → สกัดลงตัวแปร → กลับแท็บหลักรวมผล
- ต่อจากไฟล์ `26` (Tab list) + `45` (Switch/Close tab)

## 3. Variable Scope 3 ระดับ (ใหม่)
- **Global Variables:** แชร์ทุก Flow ทั้งองค์กร (เช่น URL ระบบ ERP)
- **Application Level:** ระดับแอป
- **Flow Variables:** ใช้รอบนั้นแล้วลบทิ้ง
- ใช้กับงานพี่: ค่าคงที่ (โดเมน/ชื่อตาราง) ไว้ Global, ค่ารอบส่งไว้ Flow — ไม่ปนกัน

## หมายเหตุ
- API Response/Error Codes + Work Queue/Robot + Triggers ที่ส่งมารอบนี้ซ้ำกับไฟล์ `11`/`55`/`56`/`57` — ดูไฟล์เดิม
