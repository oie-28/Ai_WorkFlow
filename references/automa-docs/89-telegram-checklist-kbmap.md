# Telegram Troubleshooting + Deployment Checklist + KB Map (ปิดท้ายคลัง)

> ที่มา: user ถอดเนื้อหามาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้
> หมายเหตุ: ส่วน Trigger/Android/Telegram พื้นฐานที่ส่งมาด้วยซ้ำกับไฟล์เดิม — ดูไฟล์ `11`/`47`/`49`/`60`/`71`/84-85

## Telegram Troubleshooting (ของใหม่)
1. **"Bad Request: media group is invalid"** — โครง `media` ไม่ถูกหรือลืมฟิลด์บังคับ (`type`/`media`):
```json
[
  {"type": "photo", "media": "https://example.com/image1.jpg", "caption": "รูปที่ 1"},
  {"type": "video", "media": "https://example.com/video1.mp4", "caption": "วิดีโอประกอบ"}
]
```
   - อ้างอิง: [Send Media Group](https://docs.goautoma.com/rpa/en-US/904212138733760512)
2. **Caption ไม่ขึ้นในอัลบั้ม** — `caption` ต้องอยู่ใน object ของสื่อแต่ละชิ้น ห้ามวางนอก Array
3. **ส่งลง Topic ผิดที่** — ต้องระบุ `messageThreadId` ตรง Topic ID ไม่งั้นลง General (ดูไฟล์ `71`)

## Deployment Checklist (ของใหม่)
| Phase | เช็ก |
|---|---|
| Development | Try-Catch จุดเสี่ยง + secret ใน Vault |
| Testing | Headless + Viewport คงที่ + ล้าง RAM/Process กันรั่ว |
| Production | Webhook แจ้ง Failed + เช็ก Credits/Proxy พอ |

## Knowledge Base Map (ภาพรวมทั้งคลัง)
| หมวด | ขอบเขต |
|---|---|
| Console & Enterprise | RBAC/API/Quota/Audit/Multi-Tenant |
| Web & Software | Scraping/Form/Pop-up/Proxy/Anti-Bot/Windows GUI |
| Android | ADB/OCR/UI Tree/ป้อนข้อความ |
| SAP | T-Code/Data Grid/Status Bar |
| AI & Multimodal | LLM/Vision/OCR/Captcha |
| Integrations | Google/Microsoft 365/Telegram/Slack/CRM/ERP |
| Data & Files | Excel-CSV/SQL/PDF-Word/FTP-SFTP |
