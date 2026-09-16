# Commands — Excel (10 คำสั่งหลัก)

> ที่มา: Commands → Excel (user ถอดเนื้อหามาให้ครบ)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## เปิด/ปิดไฟล์
1. **Open Excel workbook** — เปิด `.xlsx`/`.xls` (File Path + Visible เบื้องหลังได้ + Read-only) → workbook handle
2. **Get open Excel workbook** — เกาะไฟล์ที่เปิดอยู่แล้ว (Workbook Name เช่น `Report.xlsx`)
3. **Save Excel workbook** — Save (ทับ) / Save As (ไฟล์ใหม่ + path)
4. **Close Excel workbook** — Save before closing True/False
5. **Export Excel worksheet to PDF** — Sheet → PDF (Worksheet Name + Output Path → path ลงตัวแปร)

## วน/อ่าน/เขียน
6. **Loop through Excel worksheet content** — วนทีละแถว (Sheet + Start-End Row + Has Header) → ข้อมูลแถวลงตัวแปร
   - ตัวอย่าง: Open → Loop → Fill text field (web) → Loop ends
7. **Read Excel worksheet** — อ่านเซลล์/ช่วง (Range เช่น `A1`, `A1:C10` + Sheet) → ตัวแปร
8. **Write to Excel worksheet** — เขียนลงเซลล์เริ่ม (Start Cell + Value/Array + Sheet) → Save ตาม
9. **Count rows in Excel worksheet** — นับแถวมีข้อมูล → ตัวแปร
10. **Get first free row in Excel worksheet** — หาแถวว่างแรก → เขียนต่อท้าย
    - ตัวอย่าง: Get → `free_row` → Write (Cell `A` + free_row)

## สูตรมาตรฐาน
Open → Loop/Read → ประมวลผล → Write → Save → Close (ลืม Save/Close ไฟล์ค้างได้)
