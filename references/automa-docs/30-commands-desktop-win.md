# Commands — สายเดสก์ท็อป: Software Automation + Element (win) + Window

> ที่มา: Commands → Software Automation / Element (win) / Window (user ถอดเนื้อหามาให้ครบ)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## A. Software Automation (5 คำสั่งเปิด/สั่งโปรแกรม)

### 1. Get specified window — เกาะหน้าต่างโปรแกรม
- Match Type: Title / Process Name / Window Class / Active Window
- Match Rule: Contains / Equals / Starts with / RegEx + ชื่อหน้าต่างหรือไฟล์ (เช่น `Notepad`, `chrome.exe`)
- Output: window object-handle ลงตัวแปร
- ตัวอย่าง: Get (Title contains Calculator) → Focus window

### 2. Get list of windows — รายชื่อหน้าต่างที่เปิดอยู่
- Filter: Visible only / ทั้งหมด → Array ลงตัวแปร
- ตัวอย่าง: Get → `win_list` → For each item in list

### 3. Click Element (win) — คลิกในโปรแกรม
- Target Window + Element Selector-UI Path + Click Type (Left/Right/Double)
- ตัวอย่าง: Get window → Click ปุ่ม Save

### 4. Hover mouse over Element (win) — วางเมาส์เรียก tooltip/dropdown
- Selector + Hover duration (ms)
- ตัวอย่าง: Hover (`#FileMenu`) → Click

### 5. Fill text field (win) — พิมพ์ในโปรแกรม
- Selector + Text-Value + Clear existing text (True/False)
- ตัวอย่าง: Get (Notepad) → Fill (`Hello World`)

## B. Element (win) (9 คำสั่ง)

### 1. Drag and drop Element (win)
- Source Element → Target Element/Offset
- ตัวอย่าง: ลากไอคอนไฟล์ → โฟลเดอร์

### 2. Wait for Element (win)
- Appear/Disappear + timeout → True/False
- ตัวอย่าง: รอ 10s → Click

### 3. Fill password field (win)
- ช่องรหัส + ตัวแปรซ่อนค่า (ไม่โชว์ใน log)

### 4. Select drop-down option (win)
- Option Name/Index (เช่น `Font Size 12`)

### 5. Set checkbox state (window)
- Check/Uncheck/Toggle

### 6. Set Element value (win)
- ตั้งค่าตรงไม่ต้องพิมพ์ (เช่น `100%`)

### 7. Get Element (win)
- object/Text/Attribute → ตัวแปร (เช่น Text → `win_text` → Print)

### 8. Get related element (win)
- Anchor + Relation (Parent/Child/Sibling) → object ลงตัวแปร

### 9. Get Similar Elements (win)
- ชุด element คล้ายกัน → List (เช่น → `items_list`)

## C. Window (6 คำสั่งจัดการหน้าต่าง)
1. **Focus window** — ดึงขึ้นหน้าสุด (Get → Focus)
2. **Set window state** — Maximize/Minimize/Restore
3. **Set window visibility** — Hide/Show (ซ่อนรันเบื้องหลังแล้วค่อยโชว์)
4. **Move window** — ย้ายไปพิกัด X-Y
5. **Resize window** — ปรับกว้าง×สูง (เช่น 1920×1080)
6. **Close window** — ปิดหน้าต่างที่ระบุ

## สูตรมาตรฐานงาน win
Get specified window → Focus → Maximize → Wait for Element (Appear) → สั่งงาน → Close window
