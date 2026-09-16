# Virtual Desktop + macOS & Cross-OS (ของใหม่)

> ที่มา: user ถอดเนื้อหามาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## Virtual Desktop & Multi-Instance (ใหม่)
1. **Virtual Desktop Session** — รันบอทหลายตัวพร้อมกันเครื่องเดียว (Session Isolation แยกเมาส์/คีย์บอร์ดจากจอหลัก)
   - ตัวอย่าง: เปิด 5 เซสชันคีย์ข้อมูลพร้อมกันไม่ชนกัน
   - ต่อจาก PiP/Lock Screen (ไฟล์ 60) — ชุดรันเบื้องหลังครบ
2. **Restrictions** — ไม่รองรับแอป Single Instance (ห้ามรันซ้ำ) / แอปต้องใช้ GPU Acceleration ตรงๆ

## macOS & Cross-OS (ใหม่)
3. **macOS Capabilities** — รองรับ Web (Chrome/Safari/Firefox), Python, HTTP, Extract, File;
   จับ desktop element ได้เฉพาะแอปที่รองรับ **macOS Accessibility API** + ต้องเปิดสิทธิ์ Accessibility & Screen Recording ใน System Preferences ก่อน
4. **macOS Shell** — `Run DOS Command` / `Run Shell Script` (zsh/bash)
   - ตัวอย่าง: `screencapture -x output.png` → OCR
5. **Migrate Windows↔macOS** — Path `\` → `/` (ใช้ตัวแปรกลางจัดการ) / Hotkey `Ctrl` → `Command (⌘)`

## RDP ขั้นสูง (ใหม่ — ต่อจากไฟล์ `62`)
6. **Resolution Locking** — ล็อกในไฟล์ `.rdp`/Registry กันจอยืดหดตอนเปิด-ปิดเซสชัน
7. **Background Execution** — สั่ง `tscon` ย้าย RDP Session เข้า Console Mode ก่อนตัดเน็ต บอท UI จะได้รันต่อ
