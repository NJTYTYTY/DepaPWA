# ShrimpSense PWA - Progressive Web App

## 🚀 วิธีการใช้งาน PWA

### 1. ติดตั้งแอป (Add to Home Screen)

#### บน Android (Chrome):
1. เปิดเว็บไซต์ใน Chrome
2. กดปุ่มเมนู (⋮) ที่มุมขวาบน
3. เลือก "Add to Home screen" หรือ "ติดตั้งแอป"
4. กด "Add" หรือ "เพิ่ม"

#### บน iOS (Safari):
1. เปิดเว็บไซต์ใน Safari
2. กดปุ่ม Share (📤) ที่มุมขวาล่าง
3. เลือก "Add to Home Screen"
4. กด "Add" หรือ "เพิ่ม"

#### บน Desktop (Chrome/Edge):
1. เปิดเว็บไซต์ใน Chrome หรือ Edge
2. กดปุ่ม Install (📱) ที่ address bar
3. กด "Install" หรือ "ติดตั้ง"

### 2. คุณสมบัติ PWA

✅ **Standalone Mode**: เปิดใช้งานแบบแอปจริง ไม่มีแถบเบราว์เซอร์  
✅ **Offline Support**: ใช้งานได้แม้ไม่มีอินเทอร์เน็ต  
✅ **Push Notifications**: รับการแจ้งเตือนแบบ real-time  
✅ **Background Sync**: ซิงค์ข้อมูลเมื่อกลับมาออนไลน์  
✅ **Fast Loading**: โหลดเร็วด้วย caching system  

### 3. การทดสอบ PWA

#### ทดสอบการติดตั้ง:
1. เปิดเว็บไซต์ในเบราว์เซอร์ที่รองรับ PWA
2. ดูว่ามีปุ่ม "ติดตั้งแอป" หรือไม่
3. ทดสอบการติดตั้งลงหน้าจอหลัก

#### ทดสอบ Offline Mode:
1. ติดตั้งแอปแล้ว
2. ปิด WiFi หรือ 4G
3. เปิดแอปจากหน้าจอหลัก
4. ตรวจสอบว่ายังใช้งานได้

#### ทดสอบ Standalone Mode:
1. เปิดแอปจากหน้าจอหลัก
2. ตรวจสอบว่าไม่มีแถบเบราว์เซอร์
3. ดูเหมือนแอปมือถือจริง

### 4. ไฟล์ที่เกี่ยวข้อง

- `index.html` - หน้าเว็บหลัก
- `manifest.json` - ไฟล์กำหนดค่า PWA
- `service-worker.js` - Service Worker สำหรับ offline support
- `icons/` - ไอคอนแอปขนาดต่างๆ
- `screenshots/` - ภาพตัวอย่างแอป

### 5. การพัฒนา

#### อัปเดต Service Worker:
1. แก้ไขไฟล์ `service-worker.js`
2. อัปเดต `CACHE_NAME` ในไฟล์
3. รีเฟรชหน้าเว็บ
4. Service Worker จะอัปเดตอัตโนมัติ

#### อัปเดต Manifest:
1. แก้ไขไฟล์ `manifest.json`
2. อัปเดตข้อมูลแอป
3. รีเฟรชหน้าเว็บ

### 6. การแก้ไขปัญหา

#### แอปไม่ติดตั้ง:
- ตรวจสอบว่าเบราว์เซอร์รองรับ PWA
- ตรวจสอบ HTTPS connection
- ลองใช้เบราว์เซอร์อื่น

#### Offline ไม่ทำงาน:
- ตรวจสอบ Service Worker registration
- ดู Console ใน Developer Tools
- ลองรีเฟรชหน้าเว็บ

#### แอปไม่เปิด:
- ลบแอปเก่าออกจากหน้าจอหลัก
- ติดตั้งใหม่
- ตรวจสอบ manifest.json

## 🔧 การตั้งค่า Development

### รันบน localhost:
```bash
cd app
npm run dev
```

### ทดสอบ PWA:
1. เปิด `http://localhost:3000`
2. เปิด Developer Tools
3. ไปที่ Application tab
4. ดู Service Workers และ Manifest

### Build สำหรับ Production:
```bash
npm run build
npm start
```

## 📱 การทดสอบบนมือถือ

### ใช้ Network Tab ใน Chrome DevTools:
1. เปิด Developer Tools
2. ไปที่ Network tab
3. เลือก "Slow 3G" หรือ "Offline"
4. ทดสอบการทำงาน

### ใช้ Lighthouse:
1. เปิด Developer Tools
2. ไปที่ Lighthouse tab
3. รัน PWA audit
4. ดูคะแนนและคำแนะนำ

---

**หมายเหตุ**: PWA นี้ถูกออกแบบให้ทำงานได้ดีที่สุดบน Chrome, Edge, และ Safari ที่รองรับ PWA standards
