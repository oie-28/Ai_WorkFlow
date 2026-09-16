# Open API + Enterprise + Best Practices

> ที่มา: user ถอดเนื้อหามาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## Open API (สั่ง Automa จากข้างนอก)
1. **Run Flow via OpenAPI** — ระบบนอก (Server/Webhook) สั่งรัน Flow ผ่าน HTTP:
   API Token (Bearer) + Flow ID + Global Variables/Params (JSON) → Execution ID + Status
2. **Get Execution Logs & Status** — ตามดูผลด้วย Execution ID → ผล/เวลา/output/error logs
   - ตัวอย่าง: เรียก `/executions/{id}` → โชว์บน Dashboard นอก
   - ใช้กับงานพี่: ระบบอื่นทริกเกอร์รอบส่ง + ดึงสรุปผลไปโชว์ได้โดยไม่ต้องเปิด Automa

## Enterprise & Advanced
3. **Proxy & Anti-Detect** — Proxy (HTTP/SOCKS5 `IP:Port:User:Pass`) + Fingerprint (User-Agent/Canvas/Timezone/Geo)
   - สูตร: Set Proxy & Fingerprint → Go to URL → Scraping
   - ใช้ตอนโดนบล็อก IP/จับบอท (คู่กับ human simulation ไฟล์ 33)
4. **Credentials & Secrets Store** — เก็บ Password/Key/Token เข้ารหัส ไม่ hardcode ใน flow:
   Get Secret (`DB_PASSWORD`) → `db_pass` → Connect
   - ตรงกับ Acquire asset (ไฟล์ 38) และกฎ coding_standards

## Best Practices (2 สูตร)
5. **Dynamic Element Handling** — เว็บ AJAX/React/Vue โหลดไม่พร้อมกัน:
   Wait (Visible/Present/Network Idle) + Timeout (เช่น 10s) + Retry
6. **Task Scheduling & Triggers** — รันเองไม่ต้องกด:
   Interval (ทุก N นาที/ชม.) / Specific Time / Cron (เช่น `0 8 * * *` ทุก 08:00) / Event (Browser Startup / เข้าเว็บตาม Domain)
   - ใช้กับงานพี่: Cron ส่งรายชื่อทุกเช้า + Trigger ไฟล์ 11 ประกอบกัน
