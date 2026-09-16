# Integrations — Slack + Jira + Enterprise Messaging

> ที่มา: user ถอดเนื้อหามาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## Slack (2)
1. **Slack Triggers** — รัน flow จากเหตุการณ์: New Message / @bot Mention / File Shared
   → สกัด channel_id/user_id/message_text/file_url เข้าตัวแปร
2. **Slack Actions** — Send Message / Upload File / Create Public Channel
   - ตัวอย่าง: Schedule → Extract → Slack (รายงานประจำวัน)

## Jira (2)
3. **Issue Management** — Create/Update/Delete/Get Status (Project Key + Type Bug-Task-Story + Summary/Description/Assignee)
   - ตัวอย่าง: Try-Catch พัง → เปิด Bug Ticket อัตโนมัติ
4. **Comments & Attachments** — Add Comment / Attachment / Get Changelog
   - ตัวอย่าง: Screenshot → แนบภาพ error เข้า Issue ID

## Enterprise Messaging (2)
5. **WhatsApp Business Cloud API** — Send Text/Template/Media
   - ตัวอย่าง: HTTP รับออเดอร์ → WhatsApp ยืนยันชำระเงิน
6. **Teams & LINE** — Adaptive Cards / Flex Message เข้าช่องทีม
   - ตัวอย่าง: Task Completed → Teams สรุปผล
   - ใช้กับงานพี่: สรุปผลรอบส่งเข้า LINE Flex Message (ต่อจากไฟล์ 50/60)
