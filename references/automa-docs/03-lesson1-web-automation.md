# Lesson 1 — Web Automation (ส่งข้อความ WhatsApp)

> ที่มา: Get Started → Lesson 1 Web Automation (เนื้อหาต่อจาก General)
> ลิงก์ที่เกี่ยวข้อง: https://docs.goautoma.com/rpa/en-US/849569402005819392
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: copy-paste จากเว็บ Docs

## Overview — 2 วิธีทำ Web Automation
1. **Drag-and-Drop:** ลากแค่ 7 คำสั่งก็ส่งข้อความหาเพื่อนบน WhatsApp Web ได้
2. **Record:** ไม่ต้องลากเลย กด Record แล้วทำงานตามปกติ Automa จะสร้าง flow ให้เอง

## Prerequisites
- ติดตั้ง Automa + extension
- Login WhatsApp ในเบราว์เซอร์: https://web.whatsapp.com/

## 1. Drag and Drop
ค้นหาคำสั่งในแผงซ้ายของ Editor ลากลง Canvas ทีละอัน

> ข้อควรระวัง: คำสั่งชื่อคล้ายกันแต่ใช้ต่างกัน เช่น
> [Click Element (web)] ใช้กับเบราว์เซอร์ ส่วน [Click Element (win)] ใช้กับโปรแกรมเดสก์ท็อป

| ลำดับ | คำสั่ง | ใช้ทำอะไร |
|---|---|---|
| 1 | [Open webpage] | เปิด WhatsApp ในเบราว์เซอร์ที่ลง extension ไว้ + ใส่ URL |
| 2 | [Wait] | รอ 3 วินาทีให้เพจโหลดเสร็จ |
| 3 | [Fill text field (web)] | ค้นหาคอนแทกต์: Select + capture ช่อง "Search" แล้วกรอกชื่อ (เช่น David) |
| 4 | [Click Element (web)] | เปิดห้องแชท: capture รูป avatar ของคอนแทกต์ที่ค้นเจอ |
| 5 | [Fill text field (web)] | พิมพ์ข้อความ: capture ช่อง "Type a message" แล้วกรอกข้อความ (เช่น "Hi! Meeting time :)") |
| 6 | [Type keys] | จำลองกด Enter เพื่อส่ง (เปิด Show Keyboard Viewer → Enter) หรือใช้ [Click Element (web)] จับปุ่มส่งแทนก็ได้ |
| 7 | [Close webpage] | ปิดเพจตอนจบ (ถ้าไม่ใช้แล้ว — ลบหรือคลิกขวา disable ก็ได้) |

เสร็จแล้วกด ►Run ที่ด้านบน Editor — Automa จะส่งข้อความให้อัตโนมัติ

## 2. Record
กด Record → กด F4 เริ่มอัด → ทำงานตามปกติ (คลิก/พิมพ์) → หยุดอัด
Automa จะแปลงทุก action เป็น flow ลง Canvas ให้เอง

## หน้าถัดไป
How to send WhatsApp messages to multiple people? (ตรงกับงาน line-sent-names ของโปรเจกต์นี้)
