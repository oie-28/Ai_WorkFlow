# Engine + Branch Routing + NotebookLM (ของใหม่)

> ที่มา: user ถอดเนื้อหามาให้ (ส่วน Android/SAP/Excel/DataTable/Human ที่ส่งมาด้วยซ้ำกับไฟล์เดิม — ดูไฟล์ `32`–`35`/`47`/`68`)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## 1. Extension vs Desktop Engine (ใหม่ — สำคัญ)
- **Web Extension Engine:** รันบน Chrome Extension ตรง ไม่ต้องมี Desktop — เกาะ DOM หน้าเว็บได้ทันที เหมาะ scraping/คีย์เบราว์เซอร์
- **Storage Sync + Manifest v3:** Service Worker รันเบื้องหลังเสถียร + sync workflow ผ่าน Automa Cloud
- ใช้เลือกสถาปัตยกรรม: งานเว็บอย่างเดียวใช้ Extension พอ งานข้ามโปรแกรม/ไฟล์/DB ค่อยใช้ Desktop/Enterprise

## 2. Branch Code & Multi-Direction Routing (ใหม่)
- Branch Code / Switch Action / Evaluate Condition — แยกหลายทางตามเงื่อนไข (ไม่ใช่แค่ If 2 ทาง)
- ตัวอย่าง: Check Account Type → Branch A (VIP) / Branch B (Standard)
- ใช้กับงานพี่: แยกทางตามผลลัพธ์ (ส่งสำเร็จ/ไม่เจอคน/พัง) ชัดกว่า If ซ้อน If

## 3. NotebookLM Enterprise & AI Knowledge Base (ใหม่)
- Query Knowledge Source / Generate Summary Note / Extract Context
- ตัวอย่าง: คำถามซัพพอร์ต → NotebookLM ค้นคู่มือเทคนิค → Send Reply
- ใช้กับงานพี่: เอาคลัง Docs 63+ ไฟล์นี้เป็น knowledge base ตอบคำถาม workflow ได้
