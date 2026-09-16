# Lesson 2 — Software Automation (สั่งโปรแกรมเดสก์ท็อป)

> ที่มา: Get Started → Lesson 2 Software Automation (เนื้อหาต่อจาก Lesson 1.2)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: copy-paste จากเว็บ Docs

## Overview — 2 วิธีทำ Software Automation
1. **Drag-and-Drop:** ลากแค่ 7 คำสั่งก็ส่งข้อความผ่าน WhatsApp for Windows ได้
2. **Record:** กด Record แล้วทำงานตามปกติ Automa สร้าง flow ให้เอง

## Prerequisites
- ติดตั้ง Automa
- ติดตั้ง + login WhatsApp for Windows (https://www.whatsapp.com/)

## Steps (7 คำสั่ง — ฉบับโปรแกรมเดสก์ท็อป)
> ข้อควรระวัง: [Click Element (web)] ใช้กับเบราว์เซอร์ ส่วน [Click Element (win)] ใช้กับโปรแกรมเดสก์ท็อป

| ลำดับ | คำสั่ง | รายละเอียด |
|---|---|---|
| 1 | [Click Element (win)] | สลับไปหน้าต่างแชท: Select + capture ปุ่ม "Chats" ใน sidebar ซ้าย |
| 2 | [Click Element (win)] | เปิดหน้าค้นหาคอนแทกต์: capture ปุ่ม "New chat" |
| 3 | [Fill text field (win)] | ค้นหา: capture ช่อง "Search name or number" กรอกชื่อ (เช่น David) |
| 4 | [Click Element (win)] | เปิดห้องแชท: capture รูป "avatar" |
| 5 | [Fill text field (win)] | พิมพ์ข้อความ: capture ช่อง "Type a message" (เช่น "Hi! Meeting time :)") |
| 6 | [Input keys] | จำลองกด Enter (Show Keyboard Viewer → Enter) หรือจับปุ่มส่งด้วย [Click Element (win)] แทนก็ได้ |
| 7 | [Close window] | ปิด WhatsApp ตอนจบ (ไม่ใช้แล้วลบหรือคลิกขวา disable ได้) |

กด ►Run — Automa จะส่งข้อความผ่านแอปเดสก์ท็อปให้

## หน้าถัดไป
How to scrape data from a website and save it to an Excel file? (Lesson 3)
