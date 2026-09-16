# OpenAPI — Task History + มาตรฐาน API (Response/Status/Params/Enum)

> ที่มา: user ถอดรายละเอียด endpoint มาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## Task Execution & History (2)
1. **List Execution Records** — ประวัติรันย้อนหลังของ Task (taskId/startTime/endTime/status/page/pageSize)
   → Execution ID/Executed By/Duration/Final Status/Log Count
   - ตัวอย่าง: ดึง 7 วันย้อนหลัง → ทำรายงานสรุป
2. **Query Task & Robot Relationship** — Task ผูกกับ Robot เครื่องไหน (taskId/robotId)
   → Robot ID/Host/Online-Offline-Busy
   - ใช้เช็กเครื่อง Online ก่อนสั่งรัน

## General Notes & Specs (4)
3. **Response Format** — มาตรฐาน JSON ตอบกลับ: `code` (เช่น 0/200 = สำเร็จ) + `msg` (รายละเอียด/error) + `data` (payload)
4. **Status Codes** — 200 สำเร็จ / 401-403 token หมดอายุ-ไม่มีสิทธิ์ / 404 ไม่เจอ / 500-100xx ฝั่ง RPA (Robot Offline/Timeout/Invalid Input)
5. **Main Flow Parameters** — ส่งตัวแปรจากนอกเข้า flow ผ่าน `globalVariables`/`execParams` (Key-Value; String/Number/Boolean/Array/Nested JSON)
   - ตัวอย่าง payload: `{"variables": {"user_id": "1001", "target_url": "https://example.com"}}`
6. **Enums** — Task Status: 0 Idle / 1 Running / 2 Success / 3 Failed / 4 Stopped;
   Role: ADMIN/DEVELOPER/OPERATOR; Trigger: MANUAL/SCHEDULED/API_TRIGGER
