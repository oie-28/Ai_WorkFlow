# Commands — PDF + Word + Captcha + Database (เพิ่มเติม)

> ที่มา: user ถอดเนื้อหามาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## PDF Operations (5)
1. **Extract text from PDF** — ทั้งไฟล์/บางหน้า (All/Specific เช่น 1-3) → ตัวแปร
   - ตัวอย่าง: Extract → `pdf_text` → Extract from text (Regex หาเลขภาษี)
2. **Extract image from PDF** — รูปฝังใน PDF → โฟลเดอร์
3. **Extract pages from PDF** — ตัดบางหน้าเป็นเล่มใหม่ (เช่น 1,3,5 หรือ 2-10 → `summary.pdf`)
4. **Merge PDF files** — รวมหลายไฟล์ตามลำดับ (part1+part2 → `final_report.pdf`)
5. **Export PDF to image** — PDF → PNG/JPG (+ DPI) → ต่อ General OCR
- ใช้กับงานพี่: รวมรายงานส่งรายวัน + แปลงหลักฐานเป็นรูป/ข้อความเก็บได้

## Word Operations (2)
6. **Open Word document** — เปิด `.docx` → handle
7. **Export Word document to PDF** — Word → PDF (เช่น contract.pdf)

## Captcha Solving (1)
8. **hCaptcha / reCAPTCHA Solver** — ผ่าน Solver API (YesCaptcha/2Captcha):
   Form Checkbox Selector + รูปโจทย์ + API Key → captcha token
   - ตัวอย่าง: Click checkbox → Solver → Click Submit
   - หมายเหตุ: API Key เก็บด้วย Acquire asset (ไฟล์ 38) ห้าม hardcode

## Database — เพิ่มเติม (1)
9. **Disconnect from database** — ปิด connection (handle) หลังเสร็จ
   - สูตรเต็ม: Connect → Execute → Disconnect (ต่อจากไฟล์ 40)
