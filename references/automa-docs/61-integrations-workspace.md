# Tool Nodes — Google & Microsoft Workspace Integrations

> ที่มา: user ถอดเนื้อหามาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## 1. Google Workspace (Sheets/Drive/Gmail/Docs/Calendar/Tasks)
- ต่อ Google API ตรงไม่ต้องเขียนสคริปต์ซับซ้อน
- Input: OAuth / Service Account + Action (Read-Write Sheet, Upload Drive, Send Gmail, Create Calendar Event)
- Output: ผล API ลงตัวแปร
- ตัวอย่าง: Extract Web Data → Google Sheet (แถวใหม่) → Gmail (ยืนยัน)
- ใช้กับงานพี่: รายชื่อใน Sheets อ่าน-เขียนตรง (ต่อจากไฟล์ 60)

## 2. Microsoft 365 (Outlook/Teams/OneDrive/Dynamics CRM)
- Input: Microsoft Account Credentials + Action (Send Outlook Mail, Post Teams Message, Upload OneDrive)
- ตัวอย่าง: Process Finished → Teams Node แจ้งเตือนเข้าช่องทีม
