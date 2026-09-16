# Interface — หน้าต่างหลัก + หน้าต่าง Editor

> ที่มา: https://docs.goautoma.com/rpa/en-US/711663683285495808 (Get Started → Interface)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: copy-paste จากเว็บ Docs

## Overview
Automa มี 2 หน้าต่าง: **Main** และ **Editor**

## Main Window (เปิด Automa มาจะเจอหน้านี้ก่อน)

| ฟีเจอร์ | คำอธิบาย |
|---|---|
| App | สร้าง App ใหม่ / แก้ไข / publish / แชร์ App ที่มี |
| Trigger | สั่งรันอัตโนมัติ — กำหนดได้หลายแบบ: เวลา, ไฟล์, hotkey, อีเมล |
| Market | (TBC) ค้นหา/ดึง App สำเร็จรูปจาก Automa Official |
| Community | ปุ่มเข้า Discord — ถาม/คุยกับ dev คนอื่น/เสนอแนะ |
| Help | เปิดเอกสาร Docs |
| Me | ตั้งค่า + ติดตั้ง plug-in |

## Editor Window (กดสร้าง/แก้ไข App แล้วจะเปิดหน้านี้)
มี 6 ส่วนประกอบ:

### 1. Top Bar
| ฟีเจอร์ | คำอธิบาย |
|---|---|
| Collapse | จัดกลุ่มคำสั่งให้ดูง่าย: กด Ctrl + คลิกคำสั่งที่ต้องการ แล้วกด {三} |
| Record | วิธีสร้าง flow เร็วสุด แต่มั่นคงน้อยสุด — อัดเสร็จควรกลับมาแก้ |
| Extract Data | ขูดข้อมูลเว็บเป็นชุดแบบเร็ว |
| Built-in Browser | เบราว์เซอร์ในตัวสำหรับ web automation — ไม่ต้องลง extension + รัน headless ได้โดยไม่รบกวนงานอื่น |
| Run | รัน/หยุด flow บน Canvas ตอนนี้ |
| Debug | ไล่รันทีละคำสั่งเพื่อดีบัก |

### 2. Commands
ค้นหา + ลากคำสั่งลง Canvas กลาง — มี 2 แบบ: **Standard** (ติดมาตอนสร้าง App) และ **Custom** (ของ official/บุคคลที่สาม ติดตั้งเพิ่มได้)

### 3. Canvas
ที่ต่อ flow — ปกติรันตามลำดับ เปลี่ยนลำดับได้ด้วย flow control (loop, conditionals)
แนะนำให้กด "Try an example" ดูตัวอย่างว่าคำสั่งทำงานอย่างไร

### 4. Bottom bar
| ฟีเจอร์ | คำอธิบาย |
|---|---|
| Elements | capture element ใหม่จากเว็บ/โปรแกรม + จัดการ element ที่เคยจับไว้ |
| Images | capture รูปจากจอ + จัดการรูปที่เคยจับไว้ |
| Errors | แสดง error ของคำสั่งที่ใช้ผิดบน Canvas |
| Logs | แสดงผล [Print] + error หลังรัน flow |
| Data Table | ตารางในตัวของ Automa — เก็บข้อมูลชั่วคราว |
| Flow Arguments | ตั้ง input/output ให้ subflow — เหมือน "args" ของฟังก์ชัน Python |

### 5. Flows
จัดการ subflow, ไฟล์ Python, package, ไฟล์ resource — subflow กับไฟล์ Python ถูกเรียกจาก flow อื่นได้

### 6. Global Variables
จัดการตัวแปรกลาง — ตัวแปรที่ทุก subflow ใน App เข้าถึงได้
ตัวอย่าง: มี [Open specified webpage] หลายจุดที่ URL โดเมนเดียวกัน → เก็บโดเมนไว้ใน Global Variables แก้ที่เดียวจบ ไม่ต้องไล่แก้ทีละคำสั่ง
