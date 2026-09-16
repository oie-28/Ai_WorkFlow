# Prompt Templates — ชุดคำสั่งพื้นฐานโปรเจกต์ Ai_WorkFlow

> วิธีใช้: คัดลอกคำสั่งข้อที่ต้องการ วางต่อท้ายโจทย์ แล้วแนบไฟล์บริบท
> (`system_prompt.md` + `workflows_context.md` + `coding_standards.md`) ให้ AI ก่อนเสมอ
>
> เอกสารอ้างอิงหลัก (Automa):
> - https://docs.goautoma.com/rpa/en-US
> - https://docs.goautoma.com/rpa/en-US/710499792859115520

## หมายเหตุเกี่ยวกับ Docs
Docs ของ Automa เป็นเว็บแบบโหลดเนื้อหาด้วย JavaScript — ถ้า AI เปิดลิงก์แล้วเจอหน้าว่าง/หน้า login
ให้ยึดโครงสร้างจริงจากไฟล์ `line-flow*.automa.json` ในโปรเจกต์นี้เป็นหลัก
(Trigger → BlockBasic → BlockDelay → BlockRepeatTask → BlockLoopBreakpoint → Table/variables)

---

## 1. วิเคราะห์โจทย์ → Workflow Logic
```text
อ่าน system_prompt.md + workflows_context.md แล้ววิเคราะห์โจทย์นี้ให้หน่อย:
[วางโจทย์งานประจำตรงนี้]
ตอบเป็น 4 ส่วน: Overview Logic → Step-by-Step Plan → โครงบล็อกที่แนะนำ → วิธี Verify
ถ้าโจทย์ไม่ชัดหรือไม่ระบุเครื่องมือ (Automa/Python) ให้ถามกลับก่อน อย่าเดา
```

## 2. ออกแบบ Workflow Automa
```text
อ่าน system_prompt.md + workflows_context.md + coding_standards.md แล้วออกแบบ Automa workflow:
เป้าหมาย: [เช่น เปิด LINE Web → วนส่งข้อความหาชื่อในตาราง]
ข้อจำกัด: [เช่น หยุดเมื่อครบ maxLoop / ข้ามชื่อที่ส่งแล้วใน sentNames]
อ้างอิงบล็อกมาตรฐานจาก Docs (https://docs.goautoma.com/rpa/en-US):
Trigger, Forms/Element (pick element/click), Delay, Loop (Repeat Task + Loop Breakpoint),
Conditions, Table/Variables, Note
ส่งมอบ: ผังขั้นตอน + รายชื่อบล็อกเรียงลำดับ + ค่าตั้งต้น (delay/loop count) + จุดที่ต้อง pick element เอง
```

## 3. ดีบัก Error (Debug)
```text
Workflow นี้ error ช่วยวิเคราะห์หน่อย:
ไฟล์: [เช่น line-flow-v11.automa.json] | บล็อกที่พัง: [ชื่อ/ลำดับบล็อก]
อาการ: [เช่น ค้างที่ pick element / loop ไม่หยุด / selector หาไม่เจอ]
Log: [วางข้อความ error ตรงนี้]
ตอบ: สาเหตุที่เป็นไปได้ (เรียงตามโอกาส) → วิธีเช็คทีละข้อ → วิธีแก้ + กันไม่ให้เกิดซ้ำ
```

## 4. สร้าง/แก้สคริปต์ Python ช่วยงาน
```text
อ่าน coding_standards.md แล้วเขียน Python ตามโจทย์นี้: [อธิบายสิ่งที่ต้องการ]
ข้อบังคับ: รันเดี่ยวได้, path ด้วย pathlib, try/except มาตรฐาน,
ห้าม hardcode Token/Password (ใช้ os.getenv + placeholder เช่น {{API_KEY}})
ส่งมอบ: โค้ดเต็ม + วิธีรัน + วิธีเทสสั้นๆ
```

## 5. เขียน/อัปเดตคู่มือ (เรียกใช้คู่กับ technical_writer_instruction.md)
```text
อ่าน prompts/technical_writer_instruction.md แล้วทำตามคำสั่งในนั้น:
หัวข้อคู่มือ: [เช่น วิธีรัน line-sent-names-v11 ส่งข้อความ LINE]
แหล่งข้อมูล: [ไฟล์ workflow / โน้ต / ลิงก์ Docs]
บันทึกผลลัพธ์เป็น Markdown พร้อมส่งมอบ
```

## 6. ตรวจรับงาน (Acceptance Check)
```text
ตรวจงานนี้ตาม coding_standards.md ให้หน่อย: [วางงาน/ไฟล์]
เช็ค 4 ส่วน: Overview ตรงโจทย์ไหม → Steps ครบรันได้จริงไหม →
Code/Config ถูกมาตรฐาน + ไม่มี secret หลุดไหม → มีวิธี Verify ไหม
สรุป: ผ่าน / ไม่ผ่าน + รายการที่ต้องแก้ (ถ้ามี)
```
