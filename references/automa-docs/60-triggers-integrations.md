# Triggers + Third-Party Integrations + Value-Added

> ที่มา: user ถอดเนื้อหามาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## Triggers (4) — ตัวสั่งรัน flow
1. **Manual** — กดเอง (Studio/Extension/Console + ฟอร์มตัวแปรตั้งต้น)
2. **Schedule** — Interval / Cron (เช่น ดึงราคาน้ำมัน 06:00 ทุกวัน)
   - ใช้กับงานพี่: Cron ส่งรายชื่อทุกเช้า (ต่อจากไฟล์ 11/51)
3. **Webhook** — ระบบนอกยิง HTTP มา → รันทันที (แกะ JSON Payload ได้)
   - ตัวอย่าง: CRM มีลูกค้าใหม่ → บอททำต่อ
4. **Email** — เมลตรงเงื่อนไข (From/Subject/keyword) → รัน
   - ตัวอย่าง: หัวข้อ "ใบสั่งซื้อ" → โหลดแนบลง ERP

## Third-Party Integrations (3 กลุ่ม)
5. **Messaging & Social** — LINE/Telegram/Discord/Slack/WhatsApp Business (ข้อความ/รูป/ไฟล์)
   - ตัวอย่าง: Scraping → LINE Flex Message เข้า OA
   - ใช้กับงานพี่: สรุปผลรอบส่งเข้า LINE OA โดยตรง ไม่ต้องผ่านเบราว์เซอร์
6. **Cloud Storage & Workspace** — Sheets/Docs/Drive/OneDrive/Dropbox (อ่าน-เขียน-อัปเดตตรง ไม่ต้องเปิดเว็บ)
   - ตัวอย่าง: Extract → Google Sheets เพิ่มแถวทันที
   - ใช้กับงานพี่: รายชื่ออยู่ Google Sheets อ่าน/เขียนตรงได้เลย
7. **Productivity & CRM** — Notion/Trello/Jira/Salesforce/HubSpot/Monday
   - ตัวอย่าง: HTTP → Notion Node สร้าง Page

## Value-Added (2)
8. **Picture-in-Picture (PiP)** — รันในจอจำลองเล็ก จอหลักทำงานอื่นต่อได้ เมาส์ไม่ชนกัน
9. **Lock Screen Execution** — รันตอนล็อกจอ/Sign-out ได้ — เหมาะเครื่องรัน 24 ชม.
   - ใช้กับงานพี่: ตั้ง Cron กลางคืน + PiP/Lock Screen ไม่ต้องเฝ้าจอ (คู่กับ Disable screen saver ไฟล์ 45)
