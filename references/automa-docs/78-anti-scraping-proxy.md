# Anti-Scraping & Proxy Management

> ที่มา: user ถอดเนื้อหามาให้ (ต่อจากไฟล์ `51` Proxy & Anti-Detect)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## 1. Dynamic Proxy Rotation
- Proxy (HTTP/HTTPS/SOCKS5 + User/Pass) หมุน IP ทุก N requests หรือเมื่อเจอ `429`/`403`
- สูตร: Set Proxy → Request/Open page → Check Response → โดนบล็อก Rotate แล้วรันใหม่

## 2. Anti-Bot Bypass
- User-Agent & Fingerprint Spoofing (สุ่ม UA/Resolution/WebGL)
- Stealth: ปิด `navigator.webdriver` ให้ดูเหมือนคนจริง
- ใช้คู่กับ: human simulation (ไฟล์ `33`) + Wait สุ่ม (ไฟล์ `23`)
- ใช้กับงานพี่: ถ้า LINE เริ่มจับบอท — ครอบด้วยชุดนี้ก่อนแก้ flow
