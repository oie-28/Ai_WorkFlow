# Dialogs/OS/ConvertKit/Python — ส่วนใหม่ (ที่เหลือซ้ำไฟล์เดิม)

> ที่มา: user ถอดเนื้อหามาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้
> หมายเหตุ: Text/List/Dict, OS file พื้นฐาน, Captcha, Python พื้นฐาน, Virtual Desktop, FTP/HTTP
> ที่ส่งมารอบนี้ซ้ำกับไฟล์เดิม — ดูไฟล์ `27`/`33`/`37`–`42`/`46`/`50`/`59`/`62`/`68`/`70`

## ของใหม่รอบนี้
1. **Datetime dialog + Dropdown list dialog** — ต่อจากไฟล์ `39`/`68`:
   รับวันที่ / เลือกจาก dropdown ได้แล้ว (ไม่ใช่แค่ text/confirm/file)
2. **Zip/Unzip + Get subfolders** — ต่อจากไฟล์ `45` (File & Folder):
   บีบอัด/แตกไฟล์ + ดูโฟลเดอร์ย่อย — ใช้แพ็กรายงานรายวันได้
3. **Lock screen** — ล็อกจอด้วยคำสั่ง (คู่กับ Lock Screen Execution ไฟล์ `60`)
4. **ConvertKit** — Add Subscriber to Form / Tag / Broadcast List
   - ตัวอย่าง: Extract Lead → ConvertKit (ฟอร์มรับข่าวสาร) → Nextcloud (เอกสารต้อนรับ)
5. **Merge lists** — รวมหลาย List (ต่อจากไฟล์ `41`)
6. **Python API อีกสไตล์** — นอกจาก `automa.get_var/set_var` (ไฟล์ `59`/`62`) ยังมีแบบฟังก์ชัน:
```python
import json
data = automa_get_variable('raw_json')
processed = [item['name'] for item in json.loads(data)]
automa_set_variable('result_list', processed)
```
   - หมายเหตุ: 2 สไตล์อาจต่างเวอร์ชันกัน — ใช้ตามที่แอปพี่ยอมรับ
