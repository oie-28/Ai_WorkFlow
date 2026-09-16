# Capturing Elements — จับ + แก้ไข Element (ละเอียด)

> ที่มา: Features → Editor Window → Bottom Bar → Capturing Elements
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: copy-paste จากเว็บ Docs

## แนวคิด
Element คือชิ้นส่วนของเพจ — ต้องบอก Automa ว่าชิ้นไหนอยู่ตรงไหนถึงจะเล็งถูก
Element editor เหมือนบอก "ตา" ว่าชิ้นส่วนอยู่ตำแหน่งไหน

## What's an Element?
Element = เนื้อหาใดๆ ในเว็บ/หน้าต่างโปรแกรม (ข้อความ รูป ปุ่ม ช่องกรอก dropdown ฯลฯ)
จับแล้วสั่งงานได้: click / กรอก / ดึงข้อมูล ฯลฯ

## วิธี Capture
- จับ element ใหม่: โหมด Capture web/software element
- Deep Mode: สำหรับ element โปรแกรม (จับหน้าต่าง) — จับเว็บด้วยโหมดปกติก็ได้
- CV Intelligent Mode: ใช้ตอน 2 โหมดบนจับไม่ได้ (เช่น WeChat)
  - หมายเหตุ: จับด้วย image recognition — **แพ้ง่ายต่อความละเอียดจอ เปลี่ยนจอ/เครื่องอาจต้องจับใหม่**

## ทำไมต้อง edit element?
บางตัวจับเหมือนจะได้ แต่รันจริงเจอ "Element not found" — ต้องสร้างกฎเล็งผ่าน Element editor

> ฟีเจอร์ **AI Element Optimization**: ตอนจับ AI จะเลือก node/attribute ที่มั่นคง + สร้าง Xpath ที่ดีขึ้นให้เอง
> เปิดที่ Settings → Editor → "Use AI to generate elements when capturing"
> Enterprise Premium ใช้ไม่จำกัด / user ทั่วไปได้ **30 ครั้ง/สัปดาห์**

## วิธี edit (3 ทาง)
### 1. Default Selector (แนะนำมือใหม่)
ดูโครงเพจฝั่งซ้าย + attribute ฝั่งขวา:

| Attribute | ใช้ทำอะไร | ตัวอย่าง |
|---|---|---|
| index | ลำดับใน parent (ลูกคนที่เท่าไร) | "0" = ลูกคนแรก |
| id | identifier ไม่ซ้ำ — **มั่นคงสุด แนะนำ** | "123" |
| class | ชื่อกลุ่ม style เดียวกัน | "name" |
| innertext | ข้อความใน element — เล็งจากข้อความที่เห็น | "Automa" |
| xbox-display | element มองเห็นไหม (True/False) | "True" |

### 2. Xpath (สาย advanced — ครอบคลุม+มั่นคง+ยืดหยุ่น)
| สูตร | ความหมาย | ตัวอย่าง |
|---|---|---|
| `/` | เริ่มจาก root | `/html/body/div` |
| `//` | ค้นข้ามชั้น (ที่ไหนก็ได้) | `//div` |
| `@` | หาจากค่า attribute | `//div[@class="container"]//span[@id="title"]` |
| `text()` | หาจากข้อความ | `//button[text()="button"]` |
| `*` | wildcard | `//div/*` |
| `.` | node ปัจจุบัน | `//span` |
| `..` | parent ของ node ปัจจุบัน | `../div` |
| `[1]` | ตัวแรก (นับจาก 1) | `//ul/li[1]` |
| `[last()]` | ตัวสุดท้าย | `//ul/li[last()]` |
| `[position()<3]` | 2 ตัวแรก | `//li[position()<3]` |
| `(expr)[1]` | ตัวแรกของผลลัพธ์ | `(//div[@class="item"])[1]` |
| `[price>35]` | กรองตามเงื่อนไข | `/bookstore/book[price>35]` |

### 3. Anchor (ตัวช่วยเล็ง)
เหมือนสมอเรือ — จุดอ้างอิงที่ผูกกับ element เป้าหมาย รันจริงจะวิ่งไปหา anchor ก่อนแล้วค่อยหาเป้าหมาย
สำคัญมากตอนเป้าหมายไม่ unique (เช่น ฟอร์มมีช่องกรอกคล้ายกันหลายช่อง)

## Capturing Similar Elements
จับ 1 ตัว → กด "Capture Similar Elements" ด้านบน editor → เลือกตัวที่ 2 ที่คล้ายกัน
ระบบจะมองเป็นกลุ่ม (จอจะกะพริบ) → Save
ใช้คู่คำสั่ง batch ได้ เช่น "Loop Similar Elements" + "Click mouse" = คลิกทุกตัวในกลุ่ม

## Verify / Fix / Recapture
- **Verify Element:** เช็คว่า element ใช้ได้ไหม — กดแล้วเพจจะไฮไลต์ element ที่เจอ
- **Fix Element:** หาไม่เจอให้จับใหม่บนเพจ — AI จะสร้าง attribute ที่มั่นคงขึ้นโดยเทียบกับของเดิม
- **Recapture:** จับใหม่ทั้งตัว

## ปัญหาที่เจอบ่อย (FAQ)
1. **หา element ไม่เจอ** — สาเหตุ: (1) เลือกเพจผิด (เปิด A แต่หา element ของ B),
   (2) dynamic element (level/attribute เปลี่ยนทุกครั้งที่โหลด เช่น class สุ่ม — อย่าใช้ class ตายตัว),
   แนะนำ: edit ปรับ node/attribute หรือใส่ anchor; อาจเป็นซ่อนอยู่/โหลดนาน/iframe ซ้อน — ดู Element FAQ
2. **เจอหลายตัว** — กฎกว้างไป → จำกัด node/attribute ให้แคบลง หรือใส่ anchor
3. **จับไม่ได้เลย** — standard ไม่ได้ → In-depth mode → ยังไม่ได้ → CV mode
4. **ซ่อนอยู่จับไม่ได้** (เช่น dropdown ต้อง hover) — ลอง Ctrl+Shift+คลิกซ้าย;
   ปรับ property ผ่าน "Set Element Properties" (เช่น display:none)
5. **"Element type does not match"** — (1) จับ element ผิดฝั่ง (เอา element โปรแกรมมาใช้กับคำสั่ง web),
   (2) plug-in เพี้ยน (จับเว็บกลายเป็น software element) → refresh/reinstall plug-in แล้วจับใหม่
6. **เล็งเยื้อง (offset)** — เปลี่ยน resolution/ขนาดตัวอักษร/scale (Dpi อ่านตอน startup เปลี่ยนทีหลังแล้วเพี้ยน)

> Element เป็นภูเขาลูกยากสุดของมือใหม่ — แก้ element เป็น = ก้าวเป็น advanced developer
> ติดตรงไหนถามต่อได้ที่ Automa Discord
