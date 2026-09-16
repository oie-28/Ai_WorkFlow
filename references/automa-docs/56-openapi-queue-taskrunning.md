# OpenAPI — Work Queue + Task Running

> ที่มา: user ถอดรายละเอียด endpoint มาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## Work Queue (4) — สถาปัตยกรรมคิวงาน
1. **Add Queue Item** — เพิ่มงาน (queueId + itemData JSON + priority) → queueItemId/Queued
   - ตัวอย่าง: POST ลูกค้าใหม่ → Robot ดึงไปทำ
2. **Dequeue** — ดึงงานถัดไป (queueId + robotId) → queueItemId/itemData/Processing
   - ตัวอย่าง: Robot ว่าง → Dequeue → อ่าน itemData กรอกฟอร์ม
3. **Update Queue Items** — ปิดงาน (queueItemId + Completed/Failed + resultData/errorMessage) → success
4. **Requeue** — ส่งงานพังกลับคิว (queueItemId + reason) → newQueueItemId/Queued
   - ตัวอย่าง: Try-Catch เจอ error → Requeue ลองใหม่
- ใช้กับงานพี่: รายชื่อแต่ละคนเป็น 1 queue item — พังรายตัวไม่ล้มทั้งล็อต + retry ได้

## Task Running (4) — ควบคุมการรัน
5. **Start Task** — taskId + robotId + globalVariables → executionId (Running/Queued)
6. **Query Execution Results** — executionId → status/startTime/endTime/outputs
   - สูตร: Poll ทุก 5 วิ → Success ดึง outputs ใช้
7. **Stop Task Execution** — executionId → success (หยุดกลางคัน)
8. **Execution Callback** — ตั้ง Webhook รับผล (executionId/status/duration/resultData/errorDetails)
   - สูตร: Task จบ → Callback → อัปเดต DB หลักอัตโนมัติ (ดีกว่า Poll)
