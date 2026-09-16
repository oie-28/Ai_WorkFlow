# OpenAPI — Authentication + Enterprise Account + Organization

> ที่มา: user ถอดรายละเอียด endpoint มาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้
> หมายเหตุ: สูตรเรียกทุกตัว — ขอ token ก่อน (ข้อ 1) แล้วใส่ใน Header `Authorization` ของข้ออื่น

## 1. Authentication — ขอ Token
- Endpoint: `GET /oapi/token/v2/token/create`
- Params: `accessKeyId` + `accessKeySecret`
- Output: `accessToken` (+ `expiresIn` อายุ token)
- สูตร: HTTP Request (ส่ง Keys) → ได้ token → แปะ Header เรียก API อื่น
- ความปลอดภัย: Keys/Token เก็บด้วย Acquire asset / Secrets Store (ไฟล์ 38/51) ห้าม hardcode

## 2. Enterprise Account (5 endpoints)
| Endpoint | Params | Output | ตัวอย่าง |
|---|---|---|---|
| Query | accountId/username/page/pageSize | ID/Username/Email/Role/Status/Creation Date | HTTP → Convert text to JSON → แสดงผล |
| Create | username/email/password/role/department | accountId/status | Read CSV รายชื่อ → Loop → Create ทีละคน |
| Update | accountId/email/role/status (Enable/Disable) | success/updatedAt | ระงับสิทธิ์ |
| Delete | accountId | success | DELETE + Log |
| Reset Password | accountId/newPassword | success | Reset → Send Email แจ้งรหัสใหม่ |

## 3. Organization & Department (3)
| Endpoint | Params | Output |
|---|---|---|
| Query Dept List | deptId/deptName/page/pageSize | ID/Name/Parent/User Count — เอาไปจัดกลุ่ม user |
| Create Dept | deptName/parentId/orderNum | deptId/status (เช่น `"Automation Team"`) |
| Update/Delete Dept | deptId/deptName/parentId | success |
