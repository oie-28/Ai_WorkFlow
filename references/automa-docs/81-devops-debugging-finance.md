# DevOps + Debugging + Stripe/Odoo (ของใหม่)

> ที่มา: user ถอดเนื้อหามาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## DevOps & Docker (ใหม่)
1. **Docker** — Engine + Robot Node บน container (Linux Headless) ย้ายง่ายขยายง่าย
   - ตัวอย่าง: `docker-compose up` เปิดหลาย instance บน AWS/GCP/Azure
   - ต่อจาก HA/Restore (ไฟล์ `76`)
2. **CI/CD** — GitHub Actions/GitLab CI/Jenkins สั่ง flow (เทสหลัง build / สกัดตามเวลา)

## Debugging & Testing (ใหม่)
3. **Log Output** — Print Log ดูค่ากลางทาง / Export Log เป็นไฟล์
   - Best practice: แปะ Print ก่อนยิง API ทุกครั้ง
4. **Breakpoint & Diagnosis** — Wait/If + Screenshot ดูจอจริงตอนพัง (สำคัญมากใน Headless)
   - ใช้กับงานพี่: แปะ Print ค่าชื่อก่อนคลิกทุกครั้ง ไล่ย้อนง่าย

## Stripe/Odoo (รายละเอียดใหม่ — ต่อจากไฟล์ `66`)
5. **Stripe** — Customer/Payment Intent/Charge/Invoice
   - ตัวอย่าง: Form → ลิงก์ชำระเงิน → Telegram ส่งลูกค้า
6. **Xero/Odoo** — Sales Invoice/Stock/Journal/Purchase Order
   - ตัวอย่าง: จ่ายสำเร็จ → ลงรับชำระ + ออกใบเสร็จ

## Slack ปุ่มโต้ตอบ (ใหม่ — ต่อจากไฟล์ `65`)
7. **Interactive Buttons** — Send Channel Message + Upload File + Update Message + Handle Event
   - ตัวอย่าง: Task จบ → สรุป + Excel + ปุ่มกด (เช่น กดยืนยัน/รันซ้ำจาก Slack ได้)
