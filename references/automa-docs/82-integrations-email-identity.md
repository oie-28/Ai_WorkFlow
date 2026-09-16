# Integrations — Email + Identity + Messaging Enterprise (ของใหม่)

> ที่มา: user ถอดเนื้อหามาให้ (ส่วน Batch/Pop-up/Migration ที่ส่งมาด้วยซ้ำกับไฟล์เดิม — ดูไฟล์ `26`/`29`/`63`)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## Outlook & Email (ใหม่)
1. **Outlook** — Send/Get/Move + Download Attachments
   - ตัวอย่าง: Get (กรอง "Invoice") → Download → Extract
2. **SMTP/IMAP มาตรฐาน** — Send via SMTP / Read via IMAP / Auto-Reply
   - สูตร: Email Trigger → IMAP อ่าน → ประมวลผล → SMTP ตอบกลับ (ใช้ทำ auto-reply รายงานได้)

## Identity & ITSM (ใหม่)
3. **Okta (IAM/SSO)** — Get Profile / Assign Permission / Deactivate
   - ตัวอย่าง: BambooHR แจ้งออก → Okta ตัดสิทธิ์ทันที
4. **ServiceNow** — Create/Update Incident / Catalog Item
   - ตัวอย่าง: System Alert → Incident ด่วนอัตโนมัติ

## Messaging Enterprise (รายละเอียดใหม่ — ต่อจากไฟล์ `65`)
5. **WhatsApp Business API** — Template/Media Message + Delivery Status
   - ตัวอย่าง: Stripe Event → ใบเสร็จรูปภาพเข้า WhatsApp
6. **LINE Enterprise** — Push/Broadcast/Flex Message
   - ตัวอย่าง: Order Shipped → Flex พร้อมปุ่มติดตามพัสดุ
   - ใช้กับงานพี่: สรุปผลรอบส่งเป็นการ์ด Flex มีปุ่มได้

## SendGrid + Webflow/Stackby (ใหม่)
7. **SendGrid** — Template / Add Contact / Bounced (อีเมลปริมาณมากถึง inbox สูง)
8. **Webflow/Stackby** — CMS Item / Collection / Publish Site
   - ตัวอย่าง: Extract → Webflow (บทความใหม่ + Publish)
