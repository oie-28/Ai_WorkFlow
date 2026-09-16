# Commands — Element (10 คำสั่งจัดการ element เว็บ)

> ที่มา: Commands → Element (user ถอดเนื้อหามาให้ครบ)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## 1. Wait for Element (web) — รอ element โผล่/หาย
- Input: CSS/XPath Selector / Appear-Disappear / timeout (เช่น 10s)
- Output: True/False ลงตัวแปร
- ตัวอย่าง: Navigate → Wait (`.dashboard-content`, Appear) → Extract content

## 2. Drag and drop Element (web) — ลากวาง
- Input: Source Selector / Target Selector หรือพิกัด X-Y / Drag Speed-Delay
- ตัวอย่าง: ลาก `#item-card-1` → `#shopping-cart` → Wait 1s

## 3. Fill password field (web) — กรอกรหัสแบบปกปิด
- Input: Selector (เช่น `input[type="password"]`) / Password-Variable (masked) / Clear existing text
- ประโยชน์: ไม่โชว์รหัสใน log
- ตัวอย่าง: Fill username → Fill password (`******`) → Click

## 4. Select drop-down option (web) — เลือก dropdown
- Input: Selector (`<select>`) / Select By (Value/Label/Index) / Option Value
- ตัวอย่าง: `#country-select` By Label = Thailand

## 5. Set checkbox state (web) — ติ๊ก/เอาติ๊กออก
- Input: Selector / State (Check/Uncheck/Toggle)
- ตัวอย่าง: Check `#terms-agree` → Click `#submit`
- งานพี่: ตรงกับขั้น "ติ๊ก checkbox รายชื่อ" ใน v11 พอดี

## 6. Set Element value (web) — ตั้งค่า value ตรงๆ
- Input: Selector / Value (ข้อความ/ตัวเลข/ตัวแปร)
- ใช้ตอน: hidden field หรือช่องที่พิมพ์มือไม่ได้ผล
- ตัวอย่าง: `#date-picker` = 2026-09-16

## 7. Set Element attribute (web) — แก้ attribute
- Input: Selector / Attribute Name (disabled/style/src/href) / Attribute Value
- ตัวอย่าง: `#submit-btn` disabled = false → Click

## 8. Get Element (web) — ดึงค่า element ตัวเดียว
- Input: Selector / Get (object/Text/HTML-OuterHTML/Attribute + ชื่อ attribute)
- Output: เก็บลงตัวแปร
- ตัวอย่าง: `.price-tag` Get Text → `item_price` → Print

## 9. Get Similar Elements (web) — ดึงชุด element เป็น List
- Input: Selector ร่วม / Get (object/Text/HTML/Attribute)
- Output: List ลงตัวแปร
- ตัวอย่าง: `.product-title` → `title_list` → For each item in list

## 10. Get related Element (web) — หา element จากความสัมพันธ์ DOM
- Input: Anchor Selector / Relation (Parent/Child/Next-Previous Sibling/Ancestor/Descendant) / Target Selector-Index
- Output: เก็บ element ที่เจอลงตัวแปร
- ตัวอย่าง: Anchor `#user-row-5` + Child `.delete-btn` → Click
- ใช้ตอน: เป้าหมายไม่มี id นิ่งๆ แต่มีจุดอ้างอิงข้างๆ (คู่กับ Anchor ไฟล์ 14)
