# Commands — AI Automation: Automa AI (สนใจพิเศษ)

> ที่มา: [Automa AI](https://docs.goautoma.com/rpa/en-US/716540413654888) — user ถอดเนื้อหามาให้
> (ลิงก์ต้นฉบับ: https://docs.goautoma.com/rpa/en-US/716540413654437888)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## Automa AI
เรียกโมเดล AI (เช่น GPT-4o, GPT-4o-mini) ด้วย Prompt — สรุป/สกัดข้อมูล/แปล/วิเคราะห์รูป (Multimodal)
- Input: Model (เช่น `GPT-4o-mini`, `GPT-4o`) / Multimodal ติ๊กแนบรูป (ไฟล์ภาพ/Screenshot) / Question-Prompt
- Output: ผลตอบ AI ลงตัวแปร
- ตัวอย่าง: Get Element (web) ดึงข้อความ → Automa AI ("สกัดชื่อร้านและราคาจากข้อความนี้") → `gpt_result` → Display notification

## ใช้กับงานพี่ได้อย่างไร
- สกัดชื่อ/เบอร์จากข้อความแชทที่รูปแบบไม่นิ่ง (แทน Regex ที่พังบ่อย)
- ช่วยตัดสินใจเคสกำกวม (เช่น ข้อความนี้คือคำตอบรับหรือไม่) ก่อนบันทึกลง `sentNames`
- หมายเหตุ: มีค่าใช้จ่าย/โควตาโมเดล — งาน loop ใหญ่ควรใช้เฉพาะจุดที่กฎธรรมดาจัดการไม่ได้
