# AI FAQ + Troubleshooting + Flow extras (ของใหม่)

> ที่มา: user ถอดเนื้อหามาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## AI Service FAQ (ใหม่ — ต่อจากไฟล์ `43`/`69`)
1. **Token Management** — คุม Token รับ-ส่งกันงบ (งานสกัดใช้โมเดลเร็วถูก / งานวิเคราะห์ใช้โมเดลแม่น)
2. **Model Selection** — เลือกโมเดลตามงาน (เร็ว vs แม่น)

## Troubleshooting (ใหม่ — ต่อจากไฟล์ `62`)
3. **Browser Session** — เซสชันหลุดแก้ด้วยฉีด Cookie / เซฟ Profile (ต่อจากไฟล์ `26`)
4. **Timeout & Load** — ใช้ Dynamic Wait แทน Delay ตายตัว (ต่อจากไฟล์ `23`)

## Flow extras (ใหม่ — ต่อจากไฟล์ `40`/`44`/`69`)
5. **Try Ends + Raise** — ปิด block Try + สร้าง error จำลองเปลี่ยนทิศ flow เอง
   - สูตร: Try → Catch → Finally → Try Ends; Raise ใช้เทสทาง error โดยไม่ต้องรอพังจริง
6. **Copy resource file to clipboard** — ก๊อปไฟล์แนบลงคลิปบอร์ด (เพิ่มจาก Read/Path/Copy to folder ในไฟล์ `44`)
