# Lesson 1.2 — Message the Right Person (If / Else)

> ที่มา: https://docs.goautoma.com/rpa/en-US/849569451465052160 (Get Started → Lesson 1.2)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: copy-paste จากเว็บ Docs

## Overview
ใช้ **If / Else** ตัดสินใจตามสถานการณ์ (เจอคอนแทกต์หรือไม่เจอ)

## Prerequisites
จบ Lesson 1.1 ก่อน

## 1. Think
ถ้า Automa หาคอนแทกต์ไม่เจอจะทำอย่างไร? เช่น สะกด "Adrian" ผิดเป็น "Adrain" หรือยังไม่เคยแอดเป็นคอนแทกต์

## 2. Steps
| ลำดับ | คำสั่ง | รายละเอียด |
|---|---|---|
| 1 | [Open webpage] | เปิด WhatsApp Web |
| 2 | [Wait] | รอโหลด |
| 3 | [For each item in list] | คราวนี้ใส่ชื่อผิดปนมา เช่น `['David', 'Claire', 'Adrain']` |
| 4 | [Fill text field (web)] | ค้นหาชื่อ |
| 5 | [If Element is visible (web)] | เช็คว่า Avatar โผล่ใต้ช่อง Search ไหม — ถ้าเห็น = เจอคอนแทกต์ → คลิก + ส่งข้อความ, ถ้าไม่เห็น → ไปทาง [Else] |
| 6 | [Click Element (web)] | (กรณีเจอ) คลิก avatar |
| 7 | [Fill text field (web)] | (กรณีเจอ) พิมพ์ข้อความ |
| 8 | [Type keys] | (กรณีเจอ) Enter ส่ง |
| 9 | [Else] | ทางเลือกเมื่อไม่เข้าเงื่อนไขขั้น 5 (ไม่เห็น Avatar เช่น "Adrain") |
| 10 | [Print] | พิมพ์ชื่อที่ไม่เข้าเงื่อนไขออกมา (log ชื่อที่ส่งไม่ได้) |
| 11 | [If ends] | ถูกเพิ่มอัตโนมัติ — จุดจบ if block |
| 12 | [Loop ends] | จบ loop |
| 13 | [Close webpage] | ปิดเพจ |

กด ►Run — Automa จะส่งเฉพาะคอนแทกต์ที่มีอยู่จริง และ print ชื่อที่ไม่มีออกมา

## หน้าถัดไป
How to send messages using WhatsApp Desktop? (Lesson 2)
