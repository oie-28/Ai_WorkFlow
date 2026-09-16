# Lesson 1.1 — Message Multiple People (Loop + List)

> ที่มา: https://docs.goautoma.com/rpa/en-US/849569402005819392 (Get Started → Lesson 1.1)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: copy-paste จากเว็บ Docs

## Overview
- ใช้ **loop** ทำงานซ้ำๆ
- ใช้ **list** เก็บของที่คล้ายกัน (เช่น รายชื่อ)

## Prerequisites
จบ Lesson 1 Web Automation ก่อน

## 1. Think
จะส่งข้อความหาหลายคน (David, Kevin, Claire, ...) ได้อย่างไรโดยไม่ต้องส่งทีละคน?
- **Loop** งานที่ซ้ำ: Search ชื่อ → Click avatar → Fill ข้อความ → Enter → วนชื่อถัดไป
- **List** เก็บรายชื่อที่จะให้ Automa ไล่ทีละคน

> อ้างอิงเพิ่ม: Core Concepts — Loop; Variables — Data type — list

## 2. Steps
| ลำดับ | คำสั่ง | รายละเอียด |
|---|---|---|
| 1 | [Open webpage] | เปิด WhatsApp Web |
| 2 | [Wait] | รอโหลด |
| 3 | [For each item in list] | เริ่มวนลูป: เปิด Python mode ใส่ list ชื่อ เช่น `['David', 'Claire', 'Adrian']` — ตัวแปร `loop_item` = ชื่อรอบปัจจุบัน |
| 4 | [Fill text field (web)] | ช่องค้นหาใส่ตัวแปรแทนชื่อตายตัว (แทน "David" ด้วยตัวแปรจากขั้น 3) |
| 5 | [Click Element (web)] | คลิก avatar |
| 6 | [Fill text field (web)] | พิมพ์ข้อความ |
| 7 | [Type keys] | Enter เพื่อส่ง |
| 8 | [Loop ends] | ถูกเพิ่มอัตโนมัติ — จุดจบ loop block |
| 9 | [Close webpage] | ปิดเพจ |

กด ►Run — Automa จะส่งข้อความเดียวกันให้ทุกคนใน list

## หน้าถัดไป
What if Automa doesn't find the contact? (Lesson 1.2)
