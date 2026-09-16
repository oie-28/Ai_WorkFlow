# Element Anchors — จุดอ้างอิงช่วยเล็ง

> ที่มา: Features → Editor Window → Bottom Bar → Element Anchors
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: copy-paste จากเว็บ Docs

## Anchor คืออะไร?
จุดอ้างอิงที่ผูกกับ element เป้าหมาย — รันจริงจะวิ่งไปหา anchor ก่อนแล้วค่อยหาเป้าหมาย
เล็งนิ่งขึ้นมาก โดยเฉพาะตอนเป้าหมายไม่ unique

## วิธีทำงาน
ตอนจับ element ใส่ anchor (อัตโนมัติ/มือ) ให้มัน — anchor มักอยู่ติดกับเป้าหมายและมักเป็นข้อความนิ่งๆ
เช่น ข้อความข้างช่องกรอก หรือข้อความของ radio button
(ตัวอย่าง: ฟอร์มมีช่องกรอกคล้ายกันหลายช่อง แต่ละช่องมีข้อความกำกับข้างๆ → ข้อความนั้นถูกจับเป็น anchor อัตโนมัติ)

## ใส่ให้อัตโนมัติเมื่อไร?
| ชนิด element | หา anchor ที่ไหน |
|---|---|
| Input Box | ซ้าย + บน |
| Drop-down | ซ้าย + บน |
| Dynamic Text | รอบๆ |
| Button | ข้างใน element |
| Radio | ขวา + ล่าง |
| Checkbox | ขวา + ล่าง |

Automa จะใส่ให้เองในกรณีข้างบน — แต่ถ้าไม่มั่นใจ 100% หรือเจอของซ้ำจะไม่ใส่ให้

## ใส่มือ
หลังจับ element → Element Editor → แท็บ Anchor → Add Anchor → จับ anchor
หมายเหตุ: แนะนำเฉพาะ element ที่เล็งเดี่ยวๆ ไม่นิ่ง — **ไม่ต้องใส่ทุกตัว**
(anchor ห่วย = รันจริงหาไม่เจอ)

## ลบ Anchor
Element Editor → แท็บ Anchor → Delete Anchor

## FAQ
- **เปิด/ปิด auto anchor:** Settings → Editor → "Automatically suggest anchor points when capturing elements"
- **ทำไมไม่มีฟังก์ชัน anchor:** เช็คว่าเวอร์ชันถึงที่รองรับหรือยัง
