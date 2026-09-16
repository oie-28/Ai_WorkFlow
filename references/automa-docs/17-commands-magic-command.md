# Commands — Magic Command (สั่งด้วยแชท)

> ที่มา: Commands → Magic Command (Help Center)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: copy-paste จากเว็บ Docs

## คืออะไร
สร้างคำสั่ง web automation / data processing ด้วยการพิมพ์แชท — รองรับงานเช่น
data processing, data scraping/input
- Web Automation: component สั้นๆ (smart date picker, กรอกฟอร์ม, จัดการข้อมูลเว็บ)
- Data Processing: regex ข้อความ, Excel, list/dictionary
- Optimize Questions: บอกความต้องการไม่เก่งให้ AI ช่วยเกลาประโยค
- Smart Fix: error ตอนสร้างคำสั่งกดแก้คลิกเดียว

## ข้อดีเหนือ drag-and-drop
- สร้างง่าย: แชทอย่างเดียว ไม่ต้องมีประสบการณ์
- เก่ง: ใช้ LLM รุ่นล่าสุด — data processing + element automation นิ่งกว่า
- แก้ง่าย: Smart Fix + เห็น source code คุมเองได้หมด
- แชร์ง่าย: ส่ง source code ให้เพื่อน/community

## เหมาะกับงานแบบไหน
- Web Component (date picker, rating, pagination ที่ไม่ใช่มาตรฐาน)
- Web Process สั้นๆ (กรอกฟอร์ม, ขูดข้อมูล unstructured, loop ในเพจเดียว)
- Data Processing (list / dictionary / Excel)

## หลักการใช้ให้สำเร็จ (สำคัญ)
AI สร้างโค้ดจาก **"element region" ที่เราป้อนให้** — ป้อนไม่ครบ AI ทำไม่ได้:
- Element ต้องป้อนให้: AI สั่ง element นอกบริเวณที่ให้ไม่ได้ (เช่น dropdown/popup ที่โผล่ตอนรัน)
  ถ้า error เพราะ state เปลี่ยน เราต้องเป็น "ตาของ AI" ป้อน state ใหม่ให้
- จัด logic ด้วย Optimize Questions: ให้ AI ร่างขั้นตอน + บริเวณ element ที่อาจต้องใช้ แก้จนพอใจ

## 4 ขั้นตอน
### 1. Create a Magic Command
- เลือก Scenario: Web Automation หรือ Data Processing (ไม่เลือกจะเดาเองจากว่ามี Element Area ไหม)
- เลือก Template: พิมพ์ความต้องการตรงๆ หรือเริ่มจาก template
- บอกความต้องการ:
  - ระบุ Operation Area (เฉพาะ Web): กด Capture มุมซ้ายล่าง / แคปซูลเขียว
  - อธิบายงาน: เป้าหมาย + ขั้นตอนให้ครบที่สุด
  - Optimize Questions: ให้ AI ช่วยเกลาคำถาม
### 2. Test — กด "Run Command" มุมซ้ายล่างลองเลย
### 3. Modify (4 ทาง)
- Smart Fix: error → แก้คลิกเดียว; รันผ่านแต่ไม่ตรงใจ → สั่งแก้คลิกเดียว
- Dialogue: พิมพ์เพิ่ม/เปลี่ยนความต้องการ
- Undo: ย้อนการแก้ครั้งนี้
- Source Code: แก้โค้ดเองได้ + วาง Python สร้างคำสั่ง Automa ได้ตรงๆ
### 4. Stable Operation — สร้าง action description + หา reference ได้เหมือนคำสั่งปกติ

## FAQ
- **Capture/Verify Operation Area:** จับตามขั้น Describe; verify กดแคปซูลเปิด floating panel แล้วกด F7
- **จับบริเวณไม่ได้:** จับ element ใกล้เคียงแล้วใช้ Expand/Shrink (+ / -)
- **แชร์:** ตอนนี้แชร์ข้าม App/ข้าม user ด้วยการ "copy source code"
- **Community Edition ใช้ได้ไหม:** ได้ — โควตาแชทฟรี/สัปดาห์: Community **150 ครั้ง**, Enterprise **1,000 ครั้ง**;
  ฟีเจอร์กินทรัพยากร (เช่น Web Automation) อาจมีโควตาเพิ่มดูในแอป — ต้องการมากกว่านี้อัปเป็น Enterprise
- **แก้แล้วยัง error:** ลองเปลี่ยนประโยค / ดู source code / ถาม community (แนบ error + source code)

## Known Issues
- ยัง copy ข้าม App ไม่ได้ตรงๆ — ใช้ copy source code / custom command แทนชั่วคราว
- ยังสั่ง "Data Table" ของ Automa ไม่ได้ — จัดการตารางด้วย Excel / 2D list แทน
