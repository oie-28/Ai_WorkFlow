# Android — Environment Setup (เตรียมเครื่อง)

> ที่มา: user ถอดเนื้อหามาให้ (ต่อจากไฟล์ `47` / `49`)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## 1. Prepare for Android Automation (4 ขั้น)
1. ติดตั้งปลั๊กอิน "Android device Automation" (Avatar → Tools → Automation plug-ins)
2. เปิด Developer Mode + USB Debugging บนมือถือ
3. เสียบ USB (โหมด Transfer Files/MTP)
4. เปิด Android Manager → ยืนยันติดตั้ง Appium Settings ลงมือถือ
- สำเร็จ = เห็น Mirror Screen มือถือใน Android Manager

## 2. Mobile App Creation
- คำสั่งแรกบน Canvas ต้องเป็น `[Connect to Android device]` เลือกอุปกรณ์ที่ต่อไว้ แล้วต่อ block ควบคุมจอ
- ตัวอย่าง: Connect → Tap Element → Populate text field
