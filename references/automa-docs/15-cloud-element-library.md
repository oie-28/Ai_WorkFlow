# Cloud Element Library — แชร์ Element ข้าม App

> ที่มา: Features → Editor Window → Bottom Bar → Cloud Element Library
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: copy-paste จากเว็บ Docs

## แนวคิด
อัปโหลด element ขึ้น cloud เพื่อใช้ซ้ำข้าม App + sync realtime
ใช้ใน App ใหม่ได้โดยไม่ต้องจับใหม่ — แก้ที่เดียว App อื่นที่ผูกไว้ได้อัปเดตตาม

## Upload กลุ่ม element
คลิกขวากลุ่มใน Elements (bottom bar) → Upload to cloud

## เอา cloud element มาใช้ใน App ใหม่
1. เข้าร่วมกลุ่ม: Elements → ไอคอน cloud → เปิดกลุ่มที่ต้องการ → กลุ่มจะโผล่ใน Elements พร้อมไอคอน cloud
2. ใช้ตอนตั้งค่าคำสั่งได้ 2 แบบ:
   - เลือก cloud element ตรงๆ, หรือ
   - คลิกขวา → "Create local copy" แล้วเลือกตัวก๊อปปี้

## แก้ไขกลุ่ม cloud (ใน Elements)
- คลิกขวากลุ่ม cloud → จับ element เพิ่ม
- คลิกขวา element → edit/delete
- คลิกขวา element เดิม → ย้ายเข้ากลุ่ม cloud
- หมายเหตุ: **แก้แล้วมีผลเฉพาะ App ปัจจุบัน** — จะให้ App อื่นได้ด้วยต้องกด **"Sync"**;
  จะทิ้งที่แก้แล้วกลับไปเวอร์ชัน cloud กด **"Clear changes"**

## ลบกลุ่ม cloud
Elements → ไอคอน cloud → ... → Delete

> ⚠️ ลบแล้วเอาคืนไม่ได้ — ทุก App ที่ใช้กลุ่มนี้จะใช้ไม่ได้และอาจ error
