# Deploy + Migration + เทคนิคขูดเว็บ (ของใหม่)

> ที่มา: user ถอดเนื้อหามาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## Enterprise Deployment (ใหม่)
1. **Self-Hosted/On-Premise** — Docker Compose / Kubernetes / VM บนเครือข่ายปิด (AWS Private VPC/Azure/DC)
2. **Multi-Tenant & Billing** — แยก Workspace ตามฝ่าย (การเงิน/HR/IT) + โควตา Task Credits + รายงานแยกทีม

## Migration (รายละเอียดใหม่ — ต่อจากไฟล์ `63`)
3. **Personal → Enterprise** — ย้ายสคริปต์เข้า Workspace → เปลี่ยนตัวแปรเป็น Enterprise Assets/Credentials → ตั้ง RBAC
4. **Multi-Environment** — Export/Import + **Environment Variables Swap**
   (แยก API Key/DB connection เป็น env สลับ Dev/Staging/Prod ได้ไม่ต้องแก้ flow)

## เทคนิคขูดเว็บ (สูตรพร้อมใช้ — ต่อจากไฟล์ `63`)
5. **Lazy Loading** — Loop: Scroll ลงสุด → Wait → ครบแล้วค่อย Extract
6. **Pagination** — Wait ปุ่ม Next → สกัดลง Data Table → คลิก Next → วนจน Disabled/หาไม่เจอ
7. **Batch Media** — Get Similar Elements ดึง `src` เป็น List → วน Download/HTTP Request ลงโฟลเดอร์
