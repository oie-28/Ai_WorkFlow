# Python ขั้นสูง + FAQ & Troubleshooting

> ที่มา: user ถอดเนื้อหามาให้
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

## Python ขั้นสูง
1. **Call Process Parameters** — ดึงพารามิเตอร์ flow เข้าโค้ดผ่านโมดูล `automa`:
```python
import automa
input_data = automa.get_var("user_list")
result = [item.strip() for item in input_data]
automa.set_var("cleaned_list", result)
```
   - ใช้กับงานพี่: ล้างรายชื่อทั้งลิสต์ในครั้งเดียว (strip ช่องว่าง) ก่อนเทียบตาราง
2. **Third-Party Libraries & Custom Modules** — `pip install` (pandas/numpy/opencv/requests) + import โมดูล `.py` ของตัวเองจัดระเบียบโค้ด
   - ตัวอย่าง: Execute Python (pandas จัดตารางใหญ่) → set_var

## FAQ & Troubleshooting
3. **Web/Software FAQ** — หา element ไม่เจอ: ใช้ Selector จาก attribute นิ่ง (`data-testid`/`name`) แทน class ที่เปลี่ยนทุก build;
   อยู่ใน iframe/Shadow DOM ต้องสลับ Context เข้าไปก่อน
4. **VM/RDP FAQ** — รันบน RDP/VM: ตั้ง Registry `KeepRemoteSectionAlive` กันภาพตัดตอนพับจอ + ล็อก Resolution คงที่กันคลิกเพี้ยน
5. **SAP/Database FAQ** — เปิด Scripting ทั้ง SAP Server + GUI Client ก่อนจับ element;
   ตั้ง Connection Pool + Disconnect ทุกครั้งกัน connection รั่ว
