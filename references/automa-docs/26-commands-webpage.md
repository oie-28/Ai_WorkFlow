# Commands — Webpage (9 คำสั่งจัดการเพจ)

> ที่มา: Commands → Webpage (user ถอดเนื้อหามาให้ครบ)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## 1. Auto handle pop-ups (web) — รับมือ popup อัตโนมัติ
- Input: Action (Accept/Dismiss/Prompt text input) / Prompt Text
- ตัวอย่าง: Auto handle (Accept) → Click (จุดที่เรียก JS Alert)

## 2. Navigate to new URL — ไป URL ใหม่/ย้อน/รีเฟรช
- Input: Navigation Action (Go to URL/Back/Forward/Reload) / URL
- ตัวอย่าง: Navigate (settings URL) → Wait for page to be loaded

## 3. Wait for page to be loaded — รอเพจโหลดถึง state ที่กำหนด
- Input: Wait State (DOMContentLoaded/Complete/Network Idle) / Timeout (s)
- Output: True (โหลดทัน) / False (หมดเวลา)
- ตัวอย่าง: Click → Wait (Complete) → Extract content

## 4. Stop page loading — หยุดโหลดเพจทันที
- Input: ไม่มี / Output: ไม่มี
- ตัวอย่าง: Navigate → Wait 2s → Stop (ตัด resource หนักออก)

## 5. Scroll webpage — เลื่อนเพจ/กล่อง scroll
- Input: Scroll Action (Bottom/Top/by Pixels/to Element) / Pixel X-Y หรือ Selector / Smooth Scroll
- ตัวอย่าง: Scroll to Bottom → Wait 1s → Loop through Similar Elements (web)

## 6. Run JavaScript — รัน JS บนเพจ + รับค่ากลับ
- Input: Code Editor (โค้ด JS) / Arguments (ส่งตัวแปร Automa เข้า script)
- Output: Save return value to (ค่าจาก `return ...`)
- ตัวอย่าง: `return document.title;` → `web_title` → Print

## 7. Get list of webpages — รายชื่อแท็บที่เปิดอยู่
- Input: Scope (Current window / All browser windows)
- Output: array ของ `{tabId, title, url}` ลงตัวแปร
- ตัวอย่าง: Get → `tab_list` → For each item in list

## 8. Create cookie — เพิ่ม/อัปเดต cookie
- Input: Name / Value / Domain-Path / Flags (Secure, HttpOnly, SameSite)
- ตัวอย่าง: Create (`auth_token` = xyz123) → Navigate

## 9. Remove cookie — ลบ cookie
- Input: Remove specific cookie (by Name) / Remove all cookies + Name/Domain
- ตัวอย่าง: Remove (`session_id`) → Navigate (บังคับมุมมองแบบไม่ login)
