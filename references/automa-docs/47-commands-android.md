# Commands — Android Automation เต็มชุด

> ที่มา: user ถอดเนื้อหามาให้ (Android Automation + Android Actions)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้
> หมายเหตุ: งานปัจจุบันเป็นสายเว็บ/PC ยังไม่ใช้ Android — เก็บไว้อ้างอิง

## เชื่อมต่อ (1)
1. **Connect / Disconnect Android device** — ADB ผ่าน USB/Wi-Fi (Serial/IP:Port) → handle
   - สูตร: Connect → สั่งงาน → Disconnect

## สั่งงานพื้นฐาน (4)
2. **Tap Element / Tap** — แตะตาม Element หรือพิกัด X-Y
3. **Populate text field** — กรอกช่องในแอป (+ Append ต่อท้ายได้ เช่น `TikFlow`)
4. **Swipe** — ปัด (X1Y1 → X2Y2 + Duration ms เช่น Y 800→200 เลื่อนลง)
5. **Press button** — ปุ่มระบบ (BACK/HOME/APP_SWITCH/ENTER)

## จัดการระบบ (3)
6. **Get/Set Clipboard** — อ่าน/เขียนคลิปบอร์ด (เช่น Get → `copied_code`)
7. **Get/Set Screen Orientation** — Portrait/Landscape
8. **Take Screenshot** — Full Screen/Element → path → ต่อ Automa AI ได้

## สูตรมาตรฐาน
Connect → (Tap/Populate/Swipe) → Screenshot หลักฐาน → Disconnect
