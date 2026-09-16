# Commands — Conditionals (If / Else ทั้งตระกูล)

> ที่มา: Commands → Conditionals (หน้าย่อย If, If webpage contains, If multi-conditional,
> If Element is visible web, If window exists, If window contains, If Images exist,
> If Element exists Android, If folder exists, If file exists, Else If, Else If multi-conditional, If ends, Else)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: copy-paste จากเว็บ Docs

## โครง If block
`[If]` เปิด → `[Else If]`/`[Else]` ทางเลือก → **`[If ends]` ปิด (ห้ามลืม ไม่งั้น error)**

## If (พื้นฐาน)
- เปิด block ที่รันเมื่อเงื่อนไขตรง
- Operand 1: ปิด Python mode กรอกข้อความ / เปิด Python mode กรอก expression / จิ้มตัวแปรจากคำสั่งก่อนหน้า
- Operator: เช่น Greater than / Contains / Starts with
- Operand 2: ตั้งแบบเดียวกับ 1 (ถ้า operator มี operand เดียว เช่น Is true / Is empty ช่อง 2 จะถูกข้าม)
- ตัวอย่าง: ตั้ง int = 10 → If < 5 → Print "test 1"

## If webpage contains (เว็บมี...ไหม)
- เช็คว่าเพจมีข้อความ/Element ที่ระบุไหม
- Web page object: เลือก object จาก [Open webpage] / [Get existing webpage]
- Contains Element → เลือก/Capture Element; Contains text → กรอก "Text to check"

## If Element is visible (web) (element มองเห็นไหม)
- Web page object + เลือก Visible/Invisible + เลือก/Capture Element
- ตัวอย่าง: เปิด google.com → เช็ค "I'm Feeling Lucky" → เห็นก็คลิก

## ตารางเทียบตัวสำคัญ (จำไว้ใช้เลือกการ์ดให้ถูก)

| สถานการณ์ | webpage contains | Element is visible |
|---|---|---|
| Element โผล่ | True | True |
| Element ซ่อน | True | False |
| Similar Element set | True | True |
| Element โดนบัง | True | False |
| ข้อความบนเพจ | True | False |

> สรุป: เช็ค "มีอยู่" ใช้ contains; เช็ค "คลิกได้จริง" ใช้ visible

## If (multi-conditional) (หลายเงื่อนไข)
- Relationship: "All conditions met" (ต้องตรงทุกข้อ) / "Any condition met" (ตรงข้อเดียวก็พอ)
- Conditions: ตั้ง operand+operator ทีละข้อ กด +Add เพิ่ม
- ตัวอย่าง: string = "Automa" + int = 10 → ตรงทุกข้อ → Print "Meet all conditions" ไม่ตรง → "Doesn't meet all conditions"

## If window exists (หน้าต่างโปรแกรมมีไหม)
- หาหน้าต่างด้วย: Window object / Capture Element / Title or type name / Window handle
- Title: ใส่ชื่อหน้าต่าง (หลายหน้าต่างชื่อซ้ำ → ติ๊ก Add window type; ชื่อไม่เป๊ะ → ติ๊ก Match using wildcard เช่น `*Notepad` จับทุกชื่อที่ลงท้ายด้วย notepad)
- เลือก Exists / Does not exist
- ตัวอย่าง: เช็คหน้าต่าง "notepad" → มีก็ Get window details + Print title → ไม่มีก็ Print "Window does not exist"

## If window contains (หน้าต่างมี element ไหม)
- Window object (Match window based on targeted Element / เลือก object จาก [Get specified window])
- Contains Element / Does not contain Element + เลือก/Capture Element

## If Images exist (รูปโผล่บนจอไหม)
- Search for Image on: Entire screen / Window object / Front-most window
- Exists / Does not exist + เลือกรูปจาก Image library / Add Image (เลือกทีละหลายรูปได้)
- Wait for all Images: ติ๊ก = รอจนครบทุกรูปตามที่เลือกก่อนไปต่อ
- ตัวอย่าง: [Get specified window] → เช็ครูปครบ → Print "All targeted Images exist"

## If Element exists (Android)
- Connection object จาก [Connect to Android device] + Contains/Does not contain + เลือก/Capture Element
- ตัวอย่าง: ต่อมือถือ → เจอ element ก็ Fill in input box → ปิดด้วย [Close Android device connect]

## If folder exists / If file exists
- ใส่ absolute path (เช่น `C:\test folder`, `C:\test file.txt`) หรือเลือกจากเครื่อง
- Exists / Does not exist + Print ผล

## Else If / Else If (multi-conditional)
- Else If: ทางเลือกเมื่อ If ก่อนหน้าไม่เข้า + เงื่อนไขข้อนี้เข้า (operand/operator แบบ If)
- Else If (multi-conditional): เหมือนกันแต่เป็นลิสต์หลายเงื่อนไข (All/Any)
- ตัวอย่าง: int = 10 → If < 10 Print "Test 1" → Else If < 15 Print "Test 2" → Else Print "Test 3"

## Else
- ทางไปที่ทำเมื่อ If ก่อนหน้าไม่เข้าทุกกรณี
- ตัวอย่าง: int = 10 → If < 5 Print "Small" → Else Print "Big"

## If ends
- ปิดทุก If block — ตัวอย่าง: int = 10 → If < 5 → Print "test 1" → [End IF]
