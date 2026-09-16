# Integrations — JSON Helper + Database + Docs + Finance

> ที่มา: user ถอดเนื้อหามาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## JSON Helper (2)
1. **Parse & Query** — JSONPath/JMESPath ไม่ต้องเขียน loop
   (เช่น `$.data.orders[0].id`, `$.items[?(@.price > 100)]`) → ตัวแปร
   - ตัวอย่าง: HTTP Request → Query → Loop ต่อ
2. **Transform & Merge** — Merge objects / Filter array / Sort keys / Object→Array
   - ใช้ก่อนยิง API ปลายทาง (ต่อจาก Convert JSON ไฟล์ 42)

## Database Automation (2)
3. **Connection** — MySQL/PostgreSQL/SQL Server/Oracle (Type + Host:Port + Credentials) → Connection ID
4. **Execute & Batch Insert** — SQL ฝังตัวแปรได้ (`... WHERE status = '${user_status}'`) → Data Table/JSON
   - สูตร: Connect → Execute (`SELECT * FROM pending_tasks`) → Loop → Disconnect
   - ใช้กับงานพี่: รายชื่ออยู่ใน DB ดึงตรงได้เลย ไม่ต้องผ่านไฟล์

## PDF & Word (2)
5. **PDF Processing** — Extract Text/Images/Merge (ไม่ต้องลงโปรแกรมเพิ่ม)
   - ตัวอย่าง: Get File Path → Extract Text → Regex แกะ Tax ID
6. **Word Automation** — Open → Replace Text (`${customer_name}` → นายสมชาย) → Insert Table/Image → Export PDF → Send Email
   - ใช้กับงานพี่: ทำรายงานส่งจาก template อัตโนมัติ (ต่อจากไฟล์ 46)

## E-Commerce & Finance (2)
7. **Stripe** — Get Charge / Create Customer / Checkout Session / Verify Payment Intent
   - ตัวอย่าง: Webhook → Stripe ดึงออเดอร์ → Batch Insert DB
8. **Accounting (Xero/Quickbooks/Freshbooks)** — Create Invoice / Balances / Expense
   - ตัวอย่าง: Extract ยอดขาย → Xero สร้าง Invoice
