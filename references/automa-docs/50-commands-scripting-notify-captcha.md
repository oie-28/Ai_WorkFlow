# Commands — Scripting + Notifications + Market reCAPTCHA

> ที่มา: user ถอดเนื้อหามาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## Scripting & Code Execution
1. **Execute JavaScript** — รัน JS บนเบราว์เซอร์ จัดการ DOM/logic ซับซ้อน (อ้างตัวแปร Automa ผ่าน `automaRef` ได้) → ค่า return ลงตัวแปร
   - ตัวอย่าง: `return document.title;` → `page_title` (ท่าเดียวกับ Run JavaScript ไฟล์ 26)
2. **Execute Python / Shell** — รัน Python หรือ CMD/Bash บนเครื่อง (+ Timeout) → stdout/stderr ลงตัวแปร
   - ใช้ตอน logic เกิน block ธรรมดา (ต่อจาก Run Python script ไฟล์ 40)

## Notifications & Integration
3. **Send Email (SMTP)** — Gmail SMTP (`smtp.gmail.com:587` + App Password) + To/Subject/Body/แนบไฟล์
   - ตัวอย่าง: Export Data Table → Send Email แนบ CSV รายงาน
4. **Send Webhook (Telegram/LINE/Discord)** — POST หา Webhook/Bot API
   - ตัวอย่าง: HTTP Request → Telegram `/sendMessage` → Display notification
   - ใช้กับงานพี่: ส่งสรุปผลรอบส่งรายชื่อเข้า LINE/Telegram ได้โดยตรง

## Market Command
5. **reCAPTCHA v2/v3 Solver** — Site Key + Page URL + Solver Key (2Captcha/Anti-Captcha) → `g-recaptcha-response` token → ฉีดลงฟอร์มด้วย JS
   - เสริมจาก Captcha Solver ไฟล์ 46 (ตัวนี้เจาะ reCAPTCHA โดยเฉพาะ)
