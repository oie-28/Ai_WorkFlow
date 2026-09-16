# Integrations — Telegram & Teams ละเอียด (ของใหม่)

> ที่มา: user ถอดเนื้อหามาให้ (ต่อจากไฟล์ `50` / `60` / `65`)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## Telegram (ละเอียด)
1. **Message & Media** — Send Message/Photo/**Media Group**/Document/Video/Sticker/Location
   - Input: Chat ID + Text/File + **Parse Mode** (Markdown/HTML) + **Thread ID** (ส่งใน Topic ของ Supergroup)
   - ตัวอย่าง: Screenshot → Send Media Group (อัลบั้มหลักฐานเข้าแชท)
   - ใช้กับงานพี่: ส่งอัลบั้มหลักฐานรอบส่ง + สรุปผลจัดฟอร์แมต Markdown ได้
2. **Chat Management** — Pin/Unpin + Set Title/Description + Get Member + Leave Chat
   - ตัวอย่าง: Schedule → ปักหมุดประกาศประจำวัน

## Microsoft Teams (ละเอียด)
3. **Messaging** — Create Channel Message / Get All-Chat Msgs / Create Chat Message
   - ตัวอย่าง: Webhook → แจ้งเตือนสถานะงาน
4. **Channel & Task** — Create/Get/Delete Channel + Create/Update/Get Tasks
   - ตัวอย่าง: Extract → สร้าง Task ให้สมาชิกทีม

## หมายเหตุ
- CAPTCHA (reCAPTCHA/hCaptcha) + Account & Security API ที่ส่งมารอบนี้ซ้ำกับไฟล์ `46`/`50`/`53` — ดูไฟล์เดิม
- Android Actions ที่ส่งมารอบนี้ซ้ำกับไฟล์ `47`/`49` — ดูไฟล์เดิม
