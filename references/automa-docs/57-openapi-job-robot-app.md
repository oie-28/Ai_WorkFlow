# OpenAPI — Job/Application + Run Logs + Robot + App

> ที่มา: user ถอดรายละเอียด endpoint มาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## Job Running & Application (4)
1. **Start Application** — appId + execMode (Single/Batch) + inputParams → jobId/status
2. **Query Application Execution** — jobId → jobStatus/logs/executionDetails
3. **Stop Application Execution** — jobId → success
4. **Retry Application Execution** — jobId → newJobId (รันซ้ำพารามิเตอร์เดิมตอนพัง)

## Run Logs (1)
5. **Query Application Run Logs** — jobId + logLevel (INFO/WARN/ERROR) + page/pageSize
   → ข้อความ log + Timestamp + บรรทัดที่ error (ใช้ debug)

## Related Robot (4)
6. **Query Robot Task Queue** — robotId → Task ID ต่อคิว + ลำดับ (วางแผนกระจายโหลด)
7. **Query Robot Group List** — groupName → กลุ่ม + จำนวนสมาชิก (ส่งงานทั้ง group ได้)
8. **Query Robot List** — robotName/status (Online/Offline/Busy)/groupId → รายชื่อ + IP + งานปัจจุบัน
   - สูตร: กรอง Online + ไม่ Busy ก่อนส่งงาน
9. **Query Robot Details** — robotId → OS/CPU-RAM/Agent Version/IP (เช็กก่อนอัปสคริปต์)

## Related App (4)
10. **Query Application List** — appName/categoryId → ID/Name/Description/Version/Owner (โชว์บน Dashboard นอกได้)
11. **Query Application Run Records** — appId + ช่วงเวลา + status → Job ID/Start/End/Duration/Status
    - ตัวอย่าง: ดึง 30 วัน → คำนวณเวลาประมวลผลเฉลี่ย
12. **Query Main Flow Parameters** — appId → Parameter Name/Type/Default/Required
    - ใช้สร้างฟอร์มให้ user กรอกก่อนสั่งรัน
13. **Transfer Application Ownership** — appId + targetUserId → success (ย้ายเจ้าของตอนย้ายทีม)
