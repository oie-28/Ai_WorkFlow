# Advanced Scenarios — OS / Web / Selector / Backup

> ที่มา: user ถอดเนื้อหามาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## OS Solutions
1. **Batch/Shell Execution** — รันคำสั่ง OS (Timeout + Exit Code + Error handling)
   - ตัวอย่าง: ล้าง temp / restart service ก่อนเริ่มงาน
2. **Lazy Loading & Image Batch** — สูตร: Loop → Scroll → Wait loaded → Extract (โหลดรูป/ข้อมูลจำนวนมาก)

## Web Advanced
3. **Pagination & Infinite Scroll** — 3 ท่า: คลิก Next จน Disabled/หาไม่เจอ / วนเลข `?page=N` ใน URL / Scroll จนความสูง scrollbar ไม่เปลี่ยน
4. **Request Monitoring & Interception** — ดัก XHR/Fetch เอา JSON ตรงแทนขูด HTML:
   Start monitoring → Go to URL → Get results → Convert text to JSON (ต่อจากไฟล์ 28)
5. **Pop-up & Dialog** — Auto handle (Accept) + เช็กแท็บใหม่ → Switch tab → เสร็จ Close tab

## Selector Techniques
6. **Element Types & States** — ดูจาก HTML source: Disabled/Readonly (สั่งได้ไหม), Visible/Hidden, iFrame/Shadow DOM (สลับ Context)
7. **Regex & Variables in Selectors** — รับมือ ID เปลี่ยนทุกครั้ง:
   `input[id^="user_"]` หรือฝังตัวแปร `//div[@data-index="${loop_index}"]`
   - ใช้กับงานพี่: ห้องแชทที่ id สุ่มทุกครั้งที่โหลด — ใช้ prefix/variable แทนค่าตายตัว

## Backup & Export
8. **Export Application (.automa/JSON)** — เฉพาะ flow หรือพร้อม Variables + Assets (สำรอง/ย้ายเครื่อง)
9. **Migration to Enterprise** — นำเข้า Console → ปรับ Asset/Credential องค์กร → ตั้ง Trigger
   - เกี่ยวกับงานพี่: `line-flow*.automa.json` ที่มี = ไฟล์พร้อม migrate/export อยู่แล้ว
