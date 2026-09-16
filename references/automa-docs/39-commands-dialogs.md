# Commands — Dialogs & Notifications (2 คำสั่ง)

> ที่มา: user ถอดเนื้อหามาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

1. **Display notification** — Toast แจ้งเตือนบนจอ (Title + Message + Type: Info/Success/Warning/Error)
   - ตัวอย่าง: Task Completed (Success) — ใช้จบ loop รายงานผล
2. **Display custom dialog** — Dialog ถาม/รับค่ากลางทาง (Title/Message + Input: Text field/Dropdown/Buttons OK-Cancel)
   - Output: คำตอบผู้ใช้ลงตัวแปร
   - ตัวอย่าง: ถามรหัสยืนยัน → `user_otp` → Fill text field (web)
   - ใช้ตอน: จุดที่บอทตัดสินใจเองไม่ได้ (เช่น OTP, ยืนยันก่อนส่งล็อตใหญ่)
