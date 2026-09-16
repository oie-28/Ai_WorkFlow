# Commands — Waits ทั้ง 6 ตัว

> ที่มา: Commands → Waits (user ถอดเนื้อหาทั้งหมวดมาให้ครบ)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## หลักการร่วม
Wait แบบมีเงื่อนไข (ทุกตัวยกเว้น Wait ธรรมดา) คืน **True/False** + มี **timeout** —
หมดเวลายังไม่เกิดก็รันต่อ ใช้คู่ If/Else รับมือ (ดูไฟล์ `09-core-concepts.md` หัวข้อ Wait)

## 1. Wait for file — รอไฟล์ถูกสร้าง/ลบ
> ลิงก์: [Wait for file - Automa](https://docs.goautoma.com/rpa/en-US/716548911156932608)
- Input: File path (เช่น `C:\test file.txt`) / Wait for file to be: `Created` หรือ `Deleted` / Set timeout (s)
- Output: Save waiting result to — True (เกิดในเวลา) / False (เกินเวลา)
- ตัวอย่าง: `[Get specified webpage]` → `[HTTP download]` → `[Wait for file]` เช็คโหลดเสร็จ → True ก็ `[Print]` "Image downloaded"

## 2. Wait for Element (win) — รอ element โปรแกรมโผล่/หาย
- Input: Element selector (เดสก์ท็อป) / Wait for element to: `Appear` / `Disappear` / timeout
- Output: True/False ลงตัวแปร
- ตัวอย่าง: เปิดโปรแกรม → รอปุ่มเมนูปรากฏ → `[Click element (win)]` คลิกทันทีที่พร้อม

## 3. Wait for Element (web) — รอ element เว็บโผล่/หาย
- Input: CSS/XPath Selector / Appear (รอปุ่ม/ช่องโผล่) หรือ Disappear (รอโหลดเสร็จ/ปุ่มหาย) / timeout
- Output: True/False
- ตัวอย่าง: `[Get specified webpage]` → รอตารางโหลดเสร็จ → `[Extract content]` ดึงข้อมูล

## 4. Wait — หยุดตายตัว N วินาที
- Input: Wait time (s) — ค่าคงที่ หรือสุ่มช่วง Min-Max ได้
- Output: ไม่มี
- ตัวอย่าง: `[Click element]` → Wait 3 วิกันโดนบล็อก → `[Click element]` ต่อ

## 5. Wait for Image — รอรูปโผล่/หายบนจอ
- Input: Image target (รูปตัวอย่าง/ไฟล์รูป) / Appear / Disappear / timeout
- Output: True/False
- ตัวอย่าง: รอไอคอน Loading หายไป → ทำขั้นถัดไป

## 6. Wait for window — รอหน้าต่างเปิด/ปิด
- Input: Window title / Match rule / Wait for window to: `Exist` หรือ `Disappear` / timeout
- Output: True/False
- ตัวอย่าง: สั่งรันโปรแกรม → รอหน้าต่างเปิดสมบูรณ์ → `[Maximize window]` เต็มจอ

## สรุปเลือกใช้
| สถานการณ์ | ใช้ตัวไหน |
|---|---|
| กันโดนบล็อก/หน่วงจังหวะสั้นๆ | Wait (Min-Max สุ่มได้) |
| รอเพจ/ปุ่มพร้อม (งานเว็บ) | Wait for Element (web) + If |
| รอโปรแกรมพร้อม (งาน win) | Wait for Element (win) / Wait for window |
| รอโหลดไฟล์เสร็จ | Wait for file |
| รอ loading หาย | Wait for Image (Disappear) / Wait for Element (Disappear) |
