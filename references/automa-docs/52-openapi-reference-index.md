# OpenAPI Reference — แผนผังหมวด API ทั้งหมด

> ที่มา: user copy โครงเมนู API reference มาให้ (ต่อจากไฟล์ `51-openapi-enterprise-practices.md`)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy โครงเมนูมาให้
> หมายเหตุ: หน้านี้เป็นสารบัญ endpoint — รายละเอียดแต่ละตัว (params/response) รอ copy มาทีละหมวด

## Authentication
- Open — เปิดการยืนยันตัวตน

## RPA Enterprise Account (จัดการบัญชี)
- Query / Create / Update / Delete RPA Enterprise Account
- Reset Account Password

## Work Queue (คิวงาน)
- Requeue / Update Queue Items / Dequeue / Add Queue Item

## Task Running (รันงาน)
- Start Task
- Query Task Execution Results
- Stop Task Execution API
- Task Execution Callback

## Job Running (รันแอป)
- Start Application
- Query Application Execution
- Stop Application Execution
- Scheduled Execution Logs
- Application Execution Callback
- Retry Application Execution

## Run Logs (ประวัติ + โรบอท + แอป)
- Query Application Run Logs
- Robot: Query Task Queue / Group List / Robot List / Robot Details
- App: Query Application List / Run Records / Main Flow Parameters / Transfer Owners

## Files & Task Query
- Upload Files
- Task: Query Task & Robot Applications / Newest Execution Records /
  List Execution Records / Query Task Detail / Query Task List

## เอกสารประกอบ
- General Notes / FAQ
- Application Main Workflow Parameters
- Status Code / Response Format / Enumeration Values Descriptions

## ใช้กับงานพี่อย่างไร
- สั่งรันรอบส่งรายชื่อจากระบบนอก: Start Application/Task + ส่ง params (รายชื่อรอบนั้น)
- ตามผล: Query Execution Results / Run Logs / Callback กลับ
- คิวงาน: Add Queue Item ต่อชื่อ → Dequeue ทีละชื่อ (อีกสถาปัตยกรรมหนึ่งนอกจาก loop ใน flow)
