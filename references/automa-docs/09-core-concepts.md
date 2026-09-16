# Core Concepts — แนวคิดหลัก (App/Flow/Command/Element/Variable/Wait/Loop/If)

> ที่มา: https://docs.goautoma.com/rpa/en-US/711662346181251072 (Get Started → Core Concepts)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: copy-paste จากเว็บ Docs

## App
- คืออะไร: App สร้างเพื่อเป้าหมายหนึ่ง (เช่น "ส่งอีเมลหาลูกค้า") — ทุก App มี **Mainflow** และอาจมี **Subflow** หลายอัน
- 2 แบบ: **For PC** (สั่งเบราว์เซอร์+โปรแกรมเดสก์ท็อป) / **For Android** (สั่งมือถือ) — คำสั่งของแต่ละแบบต่างกัน
- วิธีใช้:
  - Create: New → For PC / For Android
  - Edit: ดับเบิลคลิก App ใน Main Window
  - Run: คลิกขวา App ใน Main Window → ดู logs + screen recording ได้ที่ Main Window → Trigger → Logs (เก็บดูย้อนหลังได้จนกว่าจะลบ; รันใน Editor ดู log ได้แค่ตอนเปิดอยู่ ปิดแล้วหาย)
  - Publish: คลิกขวา — **ต้อง publish ก่อน** ถึงจะแชร์หรือผูก Trigger ได้; อัปเดต+republish แล้วทุกจุดที่ใช้จะได้เวอร์ชันใหม่เอง
  - Share: คลิกขวา (ต้อง publish ก่อน)

## Flow
- คืออะไร: กลุ่มคำสั่งที่ลากลง Canvas จัดเรียงเพื่อเป้าหมายหนึ่ง
- 2 แบบ: **Mainflow** (flow หลักตอนสร้าง App) / **Subflow** (ย่อยงานซับซ้อนให้เหลือชุดเล็กๆ เรียกใช้จาก flow อื่นได้ → mainflow สั้นลง + เทสทีละส่วนได้)
- วิธีใช้:
  - สร้าง subflow: กด + บน Canvas หรือ New Flow ใน Flows
  - แก้ไข: ดับเบิลคลิก subflow ใน Flows
  - รัน: กด ►Run ทั้ง flow, หรือคลิกขวา "Run from here" รันเฉพาะส่วนหลังจุดนั้น
  - เรียกใช้: ลาก subflow จาก Flows ลง Canvas

## Command
- คืออะไร: 1 คำสั่ง = 1 action (เช่น [Print], [Open webpage]) ประกอบด้วย 4 ส่วน:
  **action** ทำบน **Element** ของ **target object** แล้วออก **result**
  - Target object: ฉากที่ element อยู่ (เพจเว็บ / หน้าต่างโปรแกรม / workbook Excel)
  - Target Element: สิ่งที่จะสั่ง (ช่องกรอก / ปุ่ม)
  - Action: คลิก / พิมพ์ / ดึงข้อมูล ฯลฯ
  - Result: คำสั่งที่มี Output จะเก็บผลลง Output variable ให้คำสั่งถัดไปใช้
- 2 แบบ: **Standard** (ติดมาตอนสร้าง App) / **Custom** (ลงเพิ่มได้)
- วิธีใช้: ลากจากแผงซ้ายลง Canvas (Create) / ดับเบิลคลิกเพื่อแก้ (Edit)

## Element
- คืออะไร: เป้าหมายที่จะสั่ง (ปุ่ม/ช่องกรอก) — capture element = บอก Automa ว่าจะทำตรงไหน
- วิธี capture ใหม่:
  1. กด Elements ที่ bottom bar (หรือกด Select ใน popup ตอนวางคำสั่ง เช่น [Click Element (web)])
  2. กด [+ Capture Element] → กด Ctrl ค้าง + คลิก element
  3. กด Verify เช็คว่าจับถูกไหม (ผิดกด Discard จับใหม่)
  4. ตั้งชื่อมีความหมาย (เช่น "Google-search-box") → Done เก็บเข้า element library
- 3 โหมด: **Standard** (ค่าเริ่มต้น ใช้ได้ส่วนใหญ่) / **In-depth** (ตอน Standard ใช้ไม่ได้) / **CV** (จับด้วย image recognition — ระวังเปลี่ยนความละเอียดจอแล้วต้องจับใหม่)
- แก้ไข: ดับเบิลคลิก element ใน Elements, หรือกด Select → hover → ไอคอน Edit element

## Similar Elements
(รายการ element ที่คล้ายกัน — ใช้คู่กับ Loop through Similar Elements)

## Variable
- คืออะไร: กล่องเก็บค่า (ตัวเลข/ข้อความ/object) มีชื่อไว้เรียกใช้
- วิธีใช้:
  - สร้างตัวแปรธรรมดา: คำสั่ง [Set variable] (ใช้ในคำสั่งถัดไปของ flow เดียวกัน) — Output ของคำสั่งก็ถูกเซฟเป็นตัวแปรเช่นกัน
  - สร้าง global: กด f+ ที่ Global Variables (ใช้ได้ทั้ง App รวม subflow อื่น)
  - แก้ค่า/ชนิด: [Set variable]
- Data expression: Automa รองรับหลายชนิด — เปิด **Python mode** (ไอคอนซ้าย) เพื่อกรอกตัวเลข (บวกลบคูณหารได้)

| ชนิด | Python mode ปิด | Python mode เปิด |
|---|---|---|
| String | Hello Automa / 123 / 1.23 | 'Hello Automa' / '123' / '1.23' |
| Number (int/decimal) | ใช้ไม่ได้ | 123 / 1.23 |
| Bool | ใช้ไม่ได้ | False / True |
| List | ใช้ไม่ได้ | ['Hello', 'Automa'] / [1,2,3] |
| Dictionary | ใช้ไม่ได้ | {'name':'Automa', 'age':1} |
| Object | สร้างได้เฉพาะจาก output ของบางคำสั่ง (เช่น webpage) | — |

## Wait
- คืออะไร: หยุด flow N วินาทีให้เงื่อนไขพร้อมก่อน (เช่น รอเพจโหลด 3 วิก่อนคลิกปุ่ม)
- 2 แบบ:
  - **[Wait]:** รอจำนวนวินาทีคงที่
  - **[Wait for something]:** รอ Element/Image/File/Window... ปรากฏ/หายไป + ตั้ง timeout ได้
    - โผล่ก่อนหมดเวลา → หยุดรอ คืน "True" รันต่อ
    - หมดเวลายังไม่โผล่ → คืน "False" รันต่อ
    - ใช้คู่ [if]/[else] รับมือแต่ละทางต่อ

## Loop
- คืออะไร: หัวใจของงานซ้ำ — วนประมวลของที่คล้ายกันหลายชิ้น / ทำ action เดิมซ้ำ
- 7 แบบ:
  1. [Loop] — ซ้ำ N รอบ (รู้จำนวนแน่นอน)
  2. [While loop] — ซ้ำจนกว่าเงื่อนไขจะเป็นจริง
  3. [Infinite loop]
  4. [Loop through Similar Elements] — วน list ของ element
  5. [Loop through Excel worksheet content] — วนเนื้อหา sheet Excel
  6. [For each item in list] — วน list (เช่น ส่งข้อความหาทุกคนใน list)
  7. [For each key-value pair in dictionary] — วน dictionary
- วิธีใช้ (โครง loop block มีอย่างน้อย 3 ส่วน):
  - Start: เลือกชนิด loop + ใส่พารามิเตอร์ (ชุดของที่จะวน)
  - Loop body: วางคำสั่งที่จะทำซ้ำระหว่าง [Loop] กับ [Loop ends]
  - End: **ต้องใส่ [Loop ends] ทุกครั้ง** ไม่งั้น error
  - ออกก่อนครบ: [Exit loop] / ข้ามรอบปัจจุบัน: [Next loop]

## If
- คืออะไร: ให้ Automa ตัดสินใจตามสถานการณ์
- แบบของ If:
  - [If] — ถ้าเงื่อนไขตรงก็ทำ...
  - [If something exists] — ถ้า Element/Image/file/folder/Window... มีอยู่ก็ทำ...
  - [If something contains] — ถ้าเพจ/หน้าต่างมี Element/ข้อความ... ก็ทำ...
  - [If (multi-conditional)] — หลายเงื่อนไขพร้อมกัน (ต้องตรงทั้งหมด/ตรงข้อใดข้อหนึ่งก็ทำ...)
- วิธีใช้: [If] / [Else If] / [Else] รับมือแต่ละกรณี
  - [If] เปิด block, [Else] รับกรณีที่ 2 (มีแค่ 2 ทาง), [Else If] รับทางที่ 3+,
  - **[If ends] ปิดทุก block ห้ามลืม** ไม่งั้น error
