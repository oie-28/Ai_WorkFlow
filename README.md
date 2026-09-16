# Ai_WorkFlow

Agent บริบท + มาตรฐานสำหรับงาน Workflow Automation

## ไฟล์หลัก
- `system_prompt.md` — บทบาท Expert Workflow & Automation Engineer + รูปแบบตอบ 4 ส่วน
- `workflows_context.md` — บริบทเครื่องมือ (Automa / Python / Beeper) + SOP
- `coding_standards.md` — มาตรฐาน Automa JSON / Python / YAML-CSV + กฎ secret safety

## วิธีใช้
1. แนบ 3 ไฟล์นี้เป็นบริบทให้ AI ก่อนสั่งงาน
2. สั่งงานสั้นๆ เช่น “อ่าน system_prompt + workflows_context แล้วออกแบบ Automa จากโจทย์...”
3. ตรวจรับตาม coding_standards (Overview → Steps → Code → Verify)

## ชุดคำสั่งพื้นฐาน (prompts/)
- `prompts/prompt_templates.md` — 6 คำสั่งพร้อมใช้: วิเคราะห์โจทย์ / ออกแบบ Automa /
  ดีบัก Error / สร้างสคริปต์ Python / เขียนคู่มือ / ตรวจรับงาน
- `prompts/technical_writer_instruction.md` — แม่แบบคำสั่งเขียนคู่มือ (อ้างอิง Automa Docs)
- วิธีเรียก: `อ่าน prompts/prompt_templates.md ข้อ 2 แล้วทำตาม: [โจทย์]`

## เอกสารอ้างอิง
- https://docs.goautoma.com/rpa/en-US
- https://docs.goautoma.com/rpa/en-US/710499792859115520
