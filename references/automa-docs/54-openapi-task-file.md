# OpenAPI — Task Execution + File Management

> ที่มา: user ถอดรายละเอียด endpoint มาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## Task & Workflow Execution (3)
1. **Query Task List & Detail** — Params: taskId/taskName/status/page/pageSize
   → Task ID/Name/Created Time/Workflow Params/Trigger Status
   - ใช้หา `taskId` ก่อนสั่งรัน
2. **Trigger / Start Task** — Params: taskId + execParams (JSON ตัวแปรตั้งต้นเข้า Flow)
   → executionId + status (Running/Queued)
   - สูตร: External Server → HTTP POST `/task/execute` → เก็บ executionId ตามผล
   - ใช้กับงานพี่: ส่งรายชื่อรอบนั้นเป็น execParams สั่งรอบส่งจากข้างนอกได้
3. **Newest Execution Records & Details** — Params: taskId/executionId
   → Start/End/Duration/Status/Error/Logs
   - สูตร: เช็ก executionId → Failed → แจ้งเตือน Telegram/LINE

## File Management (1)
4. **Upload Files** — Multipart Form-Data (file + fileType) → fileId/fileUrl/fileName
   - สูตร: Upload CSV → เอา `fileId` แนบ execParams ตอนสั่งรัน Task
   - ใช้กับงานพี่: อัปโหลดไฟล์รายชื่อรอบใหม่ → สั่งรันพร้อมกันในคำสั่งเดียว

## สูตรรวมสั่งรอบส่งจากข้างนอก
Auth (token) → Upload CSV (fileId) → Start Task (taskId + execParams) → Poll Records (executionId) → Failed แจ้งเตือน / Success ออกหลักฐาน
