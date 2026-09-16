# Enterprise — Security + HA/DR + Performance (รายละเอียดใหม่)

> ที่มา: user ถอดเนื้อหามาให้ (ต่อจากไฟล์ `58`)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## Security & Compliance (รายละเอียดใหม่)
1. **Encryption** — Data at Rest **AES-256** + Transit **TLS 1.3**;
   Credential Isolation: secret อยู่ Vault กลาง ดึงใช้เฉพาะตอนรัน ไม่โชว์ค่าดิบใน Log/สคริปต์
2. **Audit + RBAC** — ใคร/อะไร/เมื่อไร/IP; Role: Admin (ทั้งหมด) / Developer (สร้าง-แก้) /
   Operator (รันอย่างเดียว) / **Auditor** (ดูรายงาน-Log อย่างเดียว — role ใหม่)

## HA & Disaster Recovery (รายละเอียดใหม่)
3. **HA Cluster** — Load Balancer ผ่าน API Gateway/Message Broker (**Redis/RabbitMQ**) → Robot Nodes;
   **Failover**: เครื่องไหนตายคิวย้ายเอง
4. **Backup & Restore** — สำรอง Config/Task/Assets ลง **S3-Compatible** อัตโนมัติ;
   Restore ทั้งระบบบน Docker ใหม่ได้ในไม่กี่นาที

## Performance (ใหม่)
5. **Speed** — Headless + **Block Images/CSS** (เน้นข้อความ) / **API First**: มี JSON API ให้ใช้ HTTP Request ตรงเลย ไม่ต้อง render DOM
   - ใช้กับงานพี่: ถ้า LINE มี API จุดไหนยิงตรงได้จะเร็วกว่าจำลองคลิกมาก
6. **Memory** — ปิดแท็บไม่ใช้/Terminate browser ท้ายรอบกัน RAM รั่ว;
   **Batch 50–100 แถว** ก่อนเขียน DB/ยิง API (กันก้อนใหญ่ล่ม)
