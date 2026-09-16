# Commands — Mouse & Keyboard (9 คำสั่ง)

> ที่มา: Commands → Mouse & Keyboard (user ถอดเนื้อหามาให้ครบ)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## พื้นฐาน (5)
1. **Type keys** — พิมพ์/กดปุ่มลัด (`Hello World`, `{ENTER}`, `{CTRL}+C`, `{ALT}+{TAB}`)
   - ตัวอย่าง: Click mouse → Type (`{CTRL}+V`)
2. **Click mouse** — คลิกที่ปัจจุบันหรือพิกัด X-Y (Left/Right/Double)
   - ตัวอย่าง: Move mouse → Click
3. **Move mouse** — เลื่อนไป X-Y + Movement Speed
4. **Get mouse position** — พิกัดปัจจุบัน → `x_pos`, `y_pos`
5. **Scroll mouse** — หมุน wheel Up/Down + Amount

## ด้วยรูป (2)
6. **Click on Image** — หารูปบนจอแล้วคลิก (Target Image + Tolerance) → True/False
   - ตัวอย่าง: Click (`submit_button.png`) → Wait 1s
7. **Move mouse to Image** — หารูปแล้วเลื่อนเมาส์ไป (→ True/False) แล้ว Click mouse ตาม

## กันโดนจับเป็นบอท (2 — ใช้เป็นคู่)
8. **Start human simulation** — สุ่มความเร็ว/ทิศทาง/จังหวะพิมพ์ (Level Low/Medium/High)
9. **End human simulation** — กลับโหมดเร็วปกติ
- สูตร: Start → Move/Type → End

## หมายเหตุสำหรับงานพี่
- Type keys `{ENTER}` คือตัวส่งข้อความใน loop ปัจจุบัน — มีเอกสารรองรับแล้ว
- ถ้าโดนเว็บจับว่าเป็นบอท: ครอบช่วงคลิก/พิมพ์ด้วย Start–End human simulation + Wait สุ่ม Min-Max (ไฟล์ 23)
