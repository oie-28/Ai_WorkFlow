# Integrations — Enterprise CRM + Project Management (ของใหม่)

> ที่มา: user ถอดเนื้อหามาให้ (ส่วน PDF/Word/DB/Jira/GitHub/Slack ที่ส่งมาด้วยซ้ำกับไฟล์เดิม — ดูไฟล์ `46`/`54`/`65`/`67`)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## Google Workspace Ops (รายละเอียดใหม่ — ต่อจากไฟล์ `61`/`66`)
1. **Sheets** — Read/Write Cell, Get Worksheet Data, Create/Delete Worksheet, Clear Cells, Delete Rows/Columns
   - ตัวอย่าง: Extract → Sheets (ตารางสินค้าอัตโนมัติ)
2. **Calendar & Docs** — Calendar: Create/Get/Delete Event; Docs: Create/Replace Text/Export PDF
   - ตัวอย่าง: Extract Lead → Calendar (นัดประชุม) → Docs (สัญญาจาก template)

## Enterprise CRM (ใหม่)
3. **Salesforce & HubSpot** — Create/Update Lead, Get Contact, Update Deal Stage, Add Activity/Note
   - ตัวอย่าง: Webhook → Salesforce (Lead ใหม่) → HubSpot (Lifecycle Stage)
4. **Pipedrive & Freshworks** — Create/Update Deal (+Value), Get Person, Create Activity
   - ตัวอย่าง: Web Form → Pipedrive (ดีล + ยอดประเมิน)

## Project & Work (ใหม่)
5. **Trello & Monday** — Create/Move Card, Update Column, Comment/Attachment
   - ตัวอย่าง: Catch Error → Trello (Card Bug บอร์ด dev)
   - ใช้กับงานพี่: รอบส่งพังเปิดการ์ดพร้อม log อัตโนมัติได้
6. **Asana & ClickUp** — Create/Update Task, Assignee, Due Date, Subtask
   - ตัวอย่าง: Extract Order → ClickUp (Task จัดส่ง + Due)
