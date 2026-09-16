# Commands — Similar Elements ทั้ง 5 หัวข้อ

> ที่มา: Commands → Similar Elements (user ถอดเนื้อหาครบทั้งหมวดมาให้)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## แนวคิดร่วม
Element ที่โครงสร้างคล้ายกัน (รายการแชต/สินค้า/ลิงก์/แถวตาราง) จัดการเป็นชุดได้ 2 ท่า:
**Get** (ดึงทั้งชุดเก็บเป็น List ก่อน) หรือ **Loop through** (วนทำทีละตัวเลย)

## 1. Loop through Similar Elements (Android)
> ลิงก์: [Loop through Similar Elements (Android)](https://docs.goautoma.com/rpa/en-US/753213265033871360)
> วนรายการ Element บนแอป Android ทีละรายการ (เช่น รายการแชต ปุ่มในลิสต์ สินค้าในแอป)
- Input: Android device connection (จาก `Connect to Android device`) / Element ต้นแบบ (เลือกจากคลังหรือ Capture)
- Get: `Element object` (เอาไปสั่ง Click/Hover ต่อ) / `Text` / `Attribute` (Bounds + สถานะ)
- Output indices of items: ติ๊ก = ได้ index แต่ละรอบ
- Save each item to: ตัวแปรเก็บข้อมูลรอบนั้น / Loop start index (default `0` = ตัวแรก) / Loop end index (default `-1` = ตัวสุดท้าย)
- ตัวอย่าง: Connect → Loop (ดึง Element object) → Click Element (Android) ทีละรายการ → Loop ends → Close connection

## 2. Get Similar Elements (Android)
> ดึงกลุ่ม Element ที่คล้ายกันทั้งจอ Android เก็บเป็น List (ยังไม่วน)
- Input: connection / Element ต้นแบบ / Get (object/Text/Attribute)
- Save items to: ตัวแปร List เก็บผลทั้งหมด
- ตัวอย่าง: Connect → Get ลง `list_items` → Print ดูทั้งหมด

## 3. Get Similar Elements (web)
> ดึง Web Element ที่ Selector (CSS/XPath) คล้ายกันทั้งเพจเก็บเป็น List
- Input: CSS/XPath Selector ต้นแบบ / Get (object/Text/HTML-OuterHTML/Attribute)
- Save items to: ตัวแปร List
- ตัวอย่าง: Get specified webpage → Get ชื่อสินค้าทั้งหมด → บันทึกลง Data Table

## 4. Loop through Similar Elements (web)
> วน Web Element ที่โครงสร้างคล้ายกันทีละตัว (ลิงก์บทความ แถวตารางสินค้า ปุ่มหลายปุ่ม)
- Input: Selector ชุดที่จะวน / Get (object/Text/Attribute) / Output indices / Save each item to / start (`0`)–end (`-1`)
- ตัวอย่าง: Get specified webpage → Loop → Extract content ทีละตัว → Loop ends

## 5. Loop through Similar Elements (win)
> วน Element บนหน้าต่างโปรแกรม Windows ทีละตัว
- Input: Target Window/UI Element (หน้าต่าง + element ต้นแบบ) / Get (object/Text/Attribute) / Save each item to / start–end index
- ตัวอย่าง: Wait for window → Loop อ่านข้อความ/กดปุ่มทีละรายการ → Loop ends

## สรุปเลือกใช้
| ต้องการ | ใช้ตัวไหน |
|---|---|
| วนคลิก/อ่านทีละตัวบนเว็บ | Loop through (web) |
| เก็บทั้งชุดก่อนค่อยประมวล | Get (web) → List → For each / Data Table |
| งานโปรแกรม Windows | Loop through (win) |
| งานมือถือ | ตระกูล (Android) |
