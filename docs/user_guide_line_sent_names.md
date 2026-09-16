# คู่มือ: LINE ส่งข้อความรายชื่อ (line-flow-v11)

> ไฟล์ workflow: `line-flow-v11.automa.json` (ชื่อในไฟล์: "Line workflow - v11 router")
> วันที่เขียน: 2026-09-16 | เขียนจากไฟล์จริง + Docs คลัง (`references/automa-docs/`)

## 1. ภาพรวม
Workflow นี้เปิดหน้า LINE (เว็บ) วนอ่านรายชื่อเพื่อนทีละคน ข้ามชื่อที่ส่งแล้ว
ติ๊กเลือกเฉพาะชื่อใหม่ แล้วกด Send ทีเดียว จากนั้น reload แล้ววนรอบใหม่
รายชื่อที่ส่งแล้วถูกบันทึกกันส่งซ้ำ 2 ชั้น (ตัวแปร `sentNames` + ตาราง `sent_name`)

## 2. สิ่งที่ต้องเตรียม
- เบราว์เซอร์ที่ login LINE ค้างไว้แล้ว (แนะนำใช้ Profile เดิมทุกครั้ง — ดูไฟล์ `25`)
- เปิดหน้า LINE Web ให้พร้อมก่อนกดรัน
- Grant permission ที่ Automa ขอตอนรันครั้งแรก (ตามโน้ตในไฟล์)
- ตั้งค่า 2 จุดก่อนรัน: `setLoop/repeatFor` (จำนวนรอบใหญ่, ปัจจุบัน `3`) และ `loop1/maxLoop` (จำนวนคนต่อรอบ, ปัจจุบัน `7`)

## 3. ขั้นตอนการรัน (ตามลำดับบล็อก)
1. `trg1` (Trigger, manual) — จุดเริ่ม กดรันเอง
2. `act1` → `setLoop` (Repeat Task, `repeatFor=3`) — เปิดรอบใหญ่ 3 รอบ
3. `form1` — จับช่องพิมพ์ (pick element เองครั้งแรก, selector สำรอง: `textarea, [placeholder*="comment" i], div[contenteditable="true"]`)
4. `chat1` — คลิกเมนู "Chat" (XPath: `//*[normalize-space()="Chat"]`)
5. `ftab1` — คลิก tab "Friends" (XPath: `//*[normalize-space()="Friends"]`)
6. `loop1` — วนรายชื่อ (`li[class="mdCMN07Li"]`, `maxLoop=7`, loopId `round1`, รอ element นานสุด 15 วิ)
7. `getName` — อ่านชื่อรอบนี้ลงตัวแปร `currentName`
8. `normJS` (router) — ล้างช่องว่าง/เทียบตัวเล็กใหญ่กับ `sentNames`
   - ชื่อใหม่ → ไป `click1` / ชื่อซ้ำ → ข้ามไป `dly1` (ไม่คลิก)
9. `click1` — ติ๊ก checkbox/ปุ่มของแถวปัจจุบัน
10. `recJS` — เขียนชื่อลง `sentNames` (คั่นด้วย `|`) + ส่ง `{sent_name}` ลงตาราง
11. `dly1` (0.8 วิ) → `brk1` (Loop Breakpoint `round1`) → `send1` (คลิกปุ่มขึ้นต้นด้วย "Send")
12. `dly2` (30 วิ) → `reload1` (โหลดหน้าใหม่) → `dly3` (8 วิ) → วนกลับ `setLoop`
13. `export1` — Export ตารางเป็น JSON (`line-sent-names-v7`, โหมดกันชื่อซ้ำ `uniquify`)

## 4. จุดที่ต้องระวัง
- **pick element ครั้งแรก:** `form1/chat1/ftab1` ต้องจับเองกับหน้าจอจริง (Ctrl+คลิก + Verify) — ถ้า LINE เปลี่ยน UI ต้องจับใหม่ (ดูไฟล์ `13`)
- **ชื่อซ้ำเพราะช่องว่าง/ตัวพิมพ์:** router ล้างให้แล้ว (trim + เทียบ lowercase) อย่าลบโค้ดส่วนนี้
- **ค้างที่ loop1:** รายชื่อโหลดไม่ทันใน 15 วิ → เพิ่ม `waitSelectorTimeout` หรือเปลี่ยน Delay เป็น Wait for Element (ดูไฟล์ `23`)
- **onError = stop-workflow:** พังตรงไหนบอทหยุดทั้งก้อน (restart เอง 3 ครั้ง) — ถ้าอยากรันต่อข้ามจุดพัง ให้ครอบด้วย Try-Catch (ดูไฟล์ `40`)
- ตารางมีคอลัมน์เดียว (`sent_name`) — ชื่อที่อ่านได้ต้องผ่านการล้างก่อนเทียบเสมอ

## 5. วิธีตรวจผล
- เปิดตาราง workflow ดูคอลัมน์ `sent_name` — ชื่อที่ส่งแล้วต้องเพิ่มทีละแถว ไม่ซ้ำกัน
- เปิดไฟล์ export `line-sent-names-v7` (JSON) เทียบจำนวนกับที่ส่งจริง
- ดู Logs หลังรัน — ต้องไม่มี error ค้าง (settings เปิด `saveLog` + `notification` ไว้แล้ว)

## อ้างอิง
- https://docs.goautoma.com/rpa/en-US
- https://docs.goautoma.com/rpa/en-US/710499792859115520
- ไฟล์ workflow: `line-flow-v11.automa.json` (19 nodes / 19 edges)
- Docs คลัง: `04` (loop รายชื่อ), `05`+`18` (การ์ด If/visible), `21` (Next/Exit), `23` (Waits), `13`–`14` (Element/Anchor)
