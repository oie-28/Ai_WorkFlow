# Plugins/SDK + Custom Instructions + AI Vision + PiP

> ที่มา: user ถอดเนื้อหามาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## Custom Plugins & SDK
1. **Custom Plugin** — เขียน Node เอง (JS/Python/REST) โผล่ใน UI ให้ทีมลากใช้ (เช่น ต่อ Legacy/ERP ไม่มี API)
2. **SDK & External Triggering** — ฝัง Automa Engine ในแอปองค์กร (Python/Node.js) สั่งรัน + รับผลแบบ seamless

## Custom Instructions & Protection
3. **Custom Command Calling** — รวม block ใช้บ่อยเป็นคำสั่งใหม่ + ส่ง parameter แบบ dynamic → flow หลักสั้น แก้ logic กลางจุดเดียว
4. **Encoded Version & Protection** — เข้ารหัส flow (`.automa`/JSON) กันเปิดดู/ซ่อนตัวแปร/กันแกะโค้ดก่อนส่งลูกค้า

## Advanced AI & Vision
5. **Multimodal/Vision Workflows** — ส่งภาพจอ/เอกสารให้ LLM: อ่านลายมือ แยกประเภทใบเสร็จ จับจุดผิดปกติบนภาพสินค้า
   - สูตร: Screenshot → Automa AI (Vision) → JSON Helper → Database Insert
6. **Autonomous Decision Agents** — AI เลือกเส้นทาง flow เอง (Dynamic Routing) ตามหน้างานไม่แน่นอน:
   AI รับ context → คืน action ถัดไป → Automa ทำตาม
   - ใช้กับงานพี่: เคสกำกวม (ข้อความนี้ตอบรับหรือไม่) ให้ AI ตัดสินก่อนลง `sentNames`

## PiP & Screen
7. **PiP Execution** — รันในหน้าต่างแยก เมาส์/คีย์บอร์ดแยกจากจอหลัก (เทส/คีย์ข้อมูลเบื้องหลังได้ไม่ต้อง RDP)
8. **Screenshot & Viewport** — Screenshot Webpage/Element + Set Viewport คงที่ (headless จะได้เล็งตรงทุกครั้ง)
