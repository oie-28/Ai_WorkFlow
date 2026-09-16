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
- [x] Web Automation (7 คำสั่ง) → `25-commands-web-automation.md`
- [x] Webpage (9 คำสั่ง) → `26-commands-webpage.md`
- [x] Element (10 คำสั่ง) → `27-commands-element.md`
- [x] Data Extraction (12 คำสั่ง) → `28-commands-data-extraction.md`
- [x] Pop-up Handling (5 คำสั่ง) → `29-commands-popup-handling.md`
- [x] Software Automation + Element (win) + Window → `30-commands-desktop-win.md`
- [x] Data Extraction (win) → `31-commands-dataextraction-win.md`
- [x] SAP (เฉพาะทาง) → `32-commands-sap.md`
- [x] Mouse & Keyboard → `33-commands-mouse-keyboard.md`
- [x] Data Table (10 คำสั่ง) → `34-commands-data-table.md`
- [x] Excel (10 คำสั่ง) → `35-commands-excel.md`
- [x] Excel Worksheet Management (5 คำสั่ง) → `36-commands-excel-worksheet.md`
- [x] Data Processing Text+Number/Date (10 คำสั่ง) → `37-commands-data-processing.md`
- [x] Text ขั้นสูง + Variables (7 คำสั่ง) → `38-commands-data-variables.md`
- [x] Dialogs & Notifications → `39-commands-dialogs.md`
- [x] Flow Control + Network + Database + OCR/Scripting → `40-commands-flow-network-db-ocr.md`
- [x] List + Dictionary (12 คำสั่ง) → `41-commands-data-list-dict.md`
- [x] Datetime + CSV + JSON (11 คำสั่ง) → `42-commands-data-datetime-csv-json.md`
- [x] AI Automation (Automa AI) → `43-commands-ai-automation.md`
- [x] Flow (Subflow) + App & System + Resource Files → `44-commands-flow-system-resource.md`
- [x] Browser/File/Scraping ชุดรวม → `45-commands-browser-file-scrape.md`
- [x] PDF + Word + Captcha + DB เพิ่มเติม → `46-commands-pdf-word-captcha-db.md`
- [x] Android เต็มชุด → `47-commands-android.md`
- [x] OS-level + Network (ทบทวน) → `48-commands-os-network-recap.md`
- [x] Android System & Files → `49-commands-android-system.md`
- [x] Scripting + Notifications + reCAPTCHA → `50-commands-scripting-notify-captcha.md`
- [x] Open API + Enterprise + Best Practices → `51-openapi-enterprise-practices.md`
- [x] OpenAPI Reference Index (สารบัญ endpoint — รอรายละเอียดทีละหมวด) → `52-openapi-reference-index.md`
- [x] OpenAPI Auth + Account + Org → `53-openapi-auth-account.md`
- [x] OpenAPI Task Execution + File → `54-openapi-task-file.md`
- [x] OpenAPI Task History + Specs → `55-openapi-task-history-specs.md`
- [x] OpenAPI Queue + Task Running → `56-openapi-queue-taskrunning.md`
- [x] OpenAPI Job + Logs + Robot + App → `57-openapi-job-robot-app.md`
- [x] Enterprise + Console → `58-enterprise-console.md`
- [x] Python & Coding + Themes → `59-python-coding-themes.md`
- [x] Triggers + Integrations + PiP/Lock Screen → `60-triggers-integrations.md`
- [x] Google & Microsoft Workspace → `61-integrations-workspace.md`
- [x] Python ขั้นสูง + FAQ → `62-python-faq.md`
- [x] Advanced Scenarios (OS/Web/Selector/Backup) → `63-advanced-scenarios.md`
- [x] Android Setup → `64-android-setup.md`
- [x] Slack + Jira + Enterprise Messaging → `65-integrations-team.md`
- [x] JSON Helper + Database + Docs + Finance → `66-integrations-data-finance.md`
- [x] Sales/CRM + Support + Dev + Cloud CMS → `67-integrations-sales-dev.md`
- [x] Python modules + Data Types + Dialogs ขั้นสูง → `68-coding-datatypes-dialogs.md`
- [x] AI & OCR + Try-Catch-Finally (ส่วนใหม่, ที่เหลือซ้ำไฟล์เดิม) → `69-ai-ocr-finally.md`
- [x] Virtual Desktop + macOS + RDP ขั้นสูง (ของใหม่) → `70-virtual-mac-rdp.md`
- [x] Telegram & Teams ละเอียด (ของใหม่, ที่เหลือซ้ำไฟล์เดิม) → `71-telegram-teams-detail.md`
- [x] Conditionals → `18-commands-conditionals.md`
- [ ] Loops (ภาพรวม 7 แบบ + Exit/Next — รอ copy) — บันทึกแล้วเฉพาะ `Loop through Data Table` → `19-commands-loop-through-data-table.md`

## วิธีส่ง
เปิดหน้าหมวดในเบราว์เซอร์ตัวเอง → copy เนื้อหา → วางในแชท (หัวข้อความว่า "หมวด: ...")
ผมจะบันทึกเป็น `automa-docs/11-commands-<ชื่อหมวด>.md` ให้เอง
