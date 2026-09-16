# Commands — Web Automation (7 คำสั่ง)

> ที่มา: Commands → Web Automation (user ถอดเนื้อหามาให้ครบ)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## 1. Open webpage — เปิดเบราว์เซอร์ไป URL
- Input: Browser (Chrome/Edge/Firefox) / URL / Window State (Maximized/Minimized/Normal/Full screen) / Incognito mode
- Output: Save tab handle to (เก็บ tab ID ลงตัวแปร)
- ตัวอย่าง: Open (Maximized) → Wait for page to be loaded

## 2. Select Browser user — เลือกโปรไฟล์เบราว์เซอร์
- Input: Profile Path / User Name (เช่น `Profile 1`, `Default`)
- Output: ไม่มี
- ตัวอย่าง: Select (Profile 1) → Open webpage
- ประโยชน์: ใช้ session/login ค้างของโปรไฟล์นั้น ไม่ต้อง login ใหม่ทุกรอบ

## 3. Get specified webpage — เกาะแท็บที่เปิดอยู่แล้ว
- Input: Match Type (`URL`/`Title`) + Match Rule (`Contains`/`Equals`/`Starts with`/`RegEx`) + Target String (เช่น `Dashboard`)
- Output: Save active tab to
- ตัวอย่าง: Get (Title contains Dashboard) → Click Element (web)

## 4. Click Element (web) — คลิก element
- Input: Selector Type (CSS/XPath) + Selector (เช่น `#submit-btn`) / Click Type (Left/Right/Double) / Options (Scroll into view, Wait before click ms)
- Output: ไม่มี
- ตัวอย่าง: Get specified webpage → Click (`#login-button`)

## 5. Hover mouse over Element (web) — วางเมาส์เรียก hover/dropdown
- Input: Selector (เช่น `.nav-item-dropdown`) / Hover duration (ms) / Scroll into view
- Output: ไม่มี
- ตัวอย่าง: Hover (`.menu-category`) → Click (`.submenu-item`)

## 6. Fill text field (web) — กรอกช่องข้อความ
- Input: Selector (เช่น `input[name="username"]`) / Text-Value (ข้อความหรือตัวแปร) / Clear existing text (True/False) / Simulate typing (พิมพ์ทีละตัว + หน่วงเองได้)
- Output: ไม่มี
- ตัวอย่าง: Fill (`#username` = admin) → Fill (`#password`) → Click

## 7. Close webpage — ปิดแท็บ/เบราว์เซอร์
- Input: Close Scope (Current tab / Specific tab ID / All tabs)
- Output: ไม่มี
- ตัวอย่าง: Extract content → Close (Current tab)
