# Enterprise — บริหารองค์กร + Console + เสถียรภาพระบบ

> ที่มา: user ถอดเนื้อหามาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## Enterprise Management (3)
1. **Role & Permission** — สร้าง Role + สิทธิ์ Read/Write/Execute แยกแผนก/โฟลเดอร์
   (เช่น Operator กดรันได้อย่างเดียว แก้ flow ไม่ได้)
2. **Audit Logs** — ใคร/เมื่อไร/IP/คำสั่งอะไร (สร้าง-ลบ Task, แก้ secret, สลับสิทธิ์) — ใช้ย้อนรอย + Compliance
3. **License Management** — จำนวน Robot ที่ต่อได้ / วันหมดอายุ / On-Prem vs Cloud — วางแผนขยายระบบ

## Console Management (3)
4. **Asset Management** — คลังกลาง (Text/File/Credential/JSON) → Asset Key
   - ตัวอย่าง: Acquire (`API_KEY_MAIN`) → ใส่ Header HTTP (ต่อจากไฟล์ 38/51)
5. **Work Queue Management** — สร้าง/ดูสถานะ/เพิ่ม-ลบ/Retry Count/Export CSV + สถิติสำเร็จ-ล้มเหลว
6. **Wallet & Quota** — เครดิต AI/OCR/API เสริม + ประวัติตัดเครดิต + เตือนเครดิตใกล้หมด
   - เกี่ยวกับงานพี่: ใช้ Automa AI/Magic (ไฟล์ 17/43) ต้องดูโควตาตรงนี้

## Support & Troubleshooting (2)
7. **System Logs & Diagnostics** — ระดับ Debug/Info/Warn/Error + Export ส่งซัพพอร์ต
8. **Error Handling** — 3 กลยุทธ์: Retry N ครั้ง / Fallback Workflow / Alert (Webhook/Email/Telegram)
   - สูตร: Run Task → Timeout → Notify → Backup Flow (ต่อจาก Try-Catch ไฟล์ 40)

## Architecture & Deployment (2)
9. **HA & Load Balancing** — คิวกลาง + กระจายงานไป Robot Idle (รองรับ 100+ รายการ/นาที)
10. **On-Premises & Hybrid** — Air-Gapped ไม่ต่อเน็ตก็ได้ / Private Cloud ข้อมูลปลอดภัยสุด
