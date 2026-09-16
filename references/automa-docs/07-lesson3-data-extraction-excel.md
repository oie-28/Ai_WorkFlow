# Lesson 3 — Data Extraction and Storage (ขูดข้อมูลลง Excel)

> ที่มา: https://docs.goautoma.com/rpa/en-US/849569507802943488 (Get Started → Lesson 3)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: copy-paste จากเว็บ Docs

## Overview
โจทย์ตัวอย่าง: นักวิเคราะห์ต้องรีเสิร์ชตลาดด้วย Crunchbase — ให้ Automa ขูดข้อมูลจากเว็บแล้วเซฟลง Excel
- **Scrape data:** ขั้นเดียว batch ขูดหลายแถวจากเพจ
- **Save data:** เซฟลงไฟล์ Excel

## Prerequisites
- ติดตั้ง Automa + extension เบราว์เซอร์
- ติดตั้ง Microsoft Excel

## Steps
| ลำดับ | คำสั่ง | รายละเอียด |
|---|---|---|
| 1 | [Open webpage] | เปิด Crunchbase: เลือกเบราว์เซอร์ที่ลง extension + URL `https://www.crunchbase.com/` |
| 2 | [Wait] | รอ 3 วินาทีให้เพจโหลด |
| 3 | [Fill text field (web)] | capture ช่อง search กรอกหัวข้อรีเสิร์ช (เช่น "Robotics companies that might get acquired") |
| 4 | [Input keys] | Enter เริ่มค้น (หรือใช้ [Click Element (web)] จับปุ่ม send) |
| 5 | [Wait] | รอ 5 วินาทีให้ผลค้นหากลับมา |
| 6 | [Extract data] | ขูดทั้งตาราง: capture 1 cell ของตารางผลลัพธ์ → กด Capture all columns — Automa เก็บลงตัวแปร `web_data_table` |
| 7 | [Close webpage] | ปิดเพจ (ไม่ใช้แล้วลบ/disable ได้) |
| 8 | [Open Excel workbook] | สร้างไฟล์ใหม่: เลือก As new workbook + path ไฟล์ (เช่น `C:\Users*\Desktop\DataList.xlsx`) |
| 9 | [Write to Excel workbook] | เขียนข้อมูลจากขั้น 6 (กด fx เลือกตัวแปรที่เก็บข้อมูล) ลงไฟล์จากขั้น 8 |
| 10 | [Close Excel workbook] | ปิด Excel (ปกติถูกลากมาให้อัตโนมัติตอนใส่ขั้น 8) |

กด ►Run — Automa จะขูดตารางแล้วเซฟลง Excel ให้
