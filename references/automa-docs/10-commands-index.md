# Commands Index — สารบัญหมวดคำสั่งทั้งหมดใน Docs

> ที่มา: Sidebar หน้า Docs (Main Window / Editor Window / Commands)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy โครงเมนูมาให้

## โครง Docs
- Features → Main Window / Editor Window (บันทึกแล้วที่ `08-interface.md`)
- **Commands** (ยังไม่บันทึกเนื้อหา — รอ copy มาทีละหมวด):
  1. Magic Command
  2. Conditionals
  3. Loops
  4. Waits
  5. Similar Elements
  6. Web Automation
  7. Software Automation
  8. Mouse & Keyboard
  9. Data Table
  10. Excel
  11. Dialogs
  12. Data Processing
  13. OS
  14. Flow
  15. AI
  16. Network
  17. Others
  18. Android Automation
  19. Market Command

## ลำดับที่แนะนำให้ copy มาต่อ (ตามงาน line-sent-names ของโปรเจกต์)
| ลำดับ | หมวด | เหตุผล |
|---|---|---|
| 1 | Loops | งานพี่คือ loop ส่งรายชื่อ — เอารายละเอียด 7 แบบ + Exit/Next loop |
| 2 | Conditionals | การ์ดกัน element ไม่โผล่ (If Element visible + Else) |
| 3 | Waits | เปลี่ยน Delay ตายตัวเป็น Wait for something |
| 4 | Web Automation | คำสั่งเว็บละเอียด (Open/Fill/Click/Type keys) |
| 5 | Data Table | ตารางกลาง เทียบกับ `table`/`sentNames` ในไฟล์จริง |
| 6 | Excel | สำรองรายชื่อลงไฟล์ |
| 7 | Data Processing | แปลง/ล้างข้อมูลรายชื่อ |
| — | ที่เหลือ (Magic/AI/Network/OS/Flow/Dialogs/Android/Market) | ส่งมาทีหลังได้เมื่อต้องใช้ |

## สถานะการบันทึกเนื้อหา
- [x] Magic Command → `17-commands-magic-command.md`
- [x] Loops — บันทึกแล้ว: ภาพรวม 5 ตัว (`20-commands-loops-core.md`) + Loop through Data Table (`19-...`)
  เหลือ: Loop through Similar Elements, Loop through Excel worksheet content
- [x] Loop control (Next/Exit/Loop ends) → `21-commands-loops-control.md`
- [x] Loop พิเศษ (Similar Elements / Excel) → `22-commands-loops-special.md`
- [x] Waits ทั้ง 6 ตัว → `23-commands-waits.md`
- [x] Similar Elements ทั้ง 5 หัวข้อ → `24-commands-similar-elements.md`
- [x] Conditionals → `18-commands-conditionals.md`
- [ ] Loops (ภาพรวม 7 แบบ + Exit/Next — รอ copy) — บันทึกแล้วเฉพาะ `Loop through Data Table` → `19-commands-loop-through-data-table.md`

## วิธีส่ง
เปิดหน้าหมวดในเบราว์เซอร์ตัวเอง → copy เนื้อหา → วางในแชท (หัวข้อความว่า "หมวด: ...")
ผมจะบันทึกเป็น `automa-docs/11-commands-<ชื่อหมวด>.md` ให้เอง
