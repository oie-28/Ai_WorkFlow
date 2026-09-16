# Enterprise Architecture — Modular/State Machine + Governance + Maintenance

> ที่มา: user ถอดเนื้อหามาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## Modular Design & Reusable Components
- **Main-Subflow Architecture:** แยก logic หลัก/ย่อย (login / จัดการ error / แจ้งเตือน เป็น subflow)
- **Centralized Exception Handling:** รวมจัดการ error ที่ subflow กลาง แก้ที่เดียว
- ประโยชน์: ไม่ซ้ำซ้อน แก้ง่าย หลายคนทำพร้อมกันได้
- ใช้กับงานพี่: แยก `line-sent-names` เป็น main + subflow (login / ส่งรายชื่อ / บันทึกผล / แจ้งเตือน) — ต่อจากไฟล์ `44`

## State Machine & Flow Control
- ตัวแปร state คุมทิศทาง: `INIT` → `PROCESSING` → `VERIFY` → `SUCCESS` / `ERROR`
- ใช้ตอน flow มีสถานะซับซ้อน (เช่น คำสั่งซื้อเปลี่ยนตามจ่ายเงิน/จัดส่ง)
- ใช้กับงานพี่: state รายชื่อ (รอส่ง/ส่งแล้ว/ส่งพัง/ข้าม) แทนการจำด้วยตารางอย่างเดียว

## Governance, Monitoring & SLA
- **Dashboard:** Success Rate / Avg Execution Time / Queue Backlog + แจ้งเตือนผ่าน Webhook (Slack/LINE/Telegram/Email) เมื่อต่ำกว่าเกณฑ์
- **SLA:** Queue Priority (High/Medium/Low) งานด่วนรันก่อน + เตือนก่อนคิวค้างเกิน SLA

## Maintenance & Versioning
- **Versioning & Rollback:** เก็บประวัติแก้ flow + Diff + Rollback (ต่อจาก `line-flow` v7–v11 ของพี่ที่มีอยู่ — ทำแบบเดียวกันบน Enterprise ได้ในระบบ)
- **Checklist:** ล้าง log เก่า (Retention) / เช็ก Token-Session หมดอายุ / อัปเดต Selector เมื่อเว็บเปลี่ยน UI
