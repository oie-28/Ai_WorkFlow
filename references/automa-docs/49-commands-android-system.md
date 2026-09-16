# Commands — Android System & File Operations (เพิ่มเติม)

> ที่มา: user ถอดเนื้อหามาให้ (ต่อจากไฟล์ `47-commands-android.md`)
> วันที่บันทึก: 2026-09-16 | วิธีบันทึก: user copy + สรุปมาให้

1. **Get UI tree** — ดึงโครง UI ทั้งจอ (Hierarchy/XML Tree) → ตัวแปร (`ui_xml`)
   - ใช้หา Selector ปุ่ม/ข้อความ → ต่อ Automa AI วิเคราะห์พิกัดได้
2. **Get/Push file** — ดึงไฟล์จากมือถือลงคอม หรือดันไฟล์จากคอมเข้ามือถือ
   - Remote Path (เช่น `/sdcard/Download/photo.jpg`) ↔ Local Path
   - ตัวอย่าง: Screenshot (Android) → Get file ลงเครื่อง
3. **App Management** — Launch/Stop/Install/Uninstall (Package Name เช่น `com.instagram.android`, APK path)
   - ตัวอย่าง: Launch (`com.ss.android.ugc.trill`) → Delay → Tap
