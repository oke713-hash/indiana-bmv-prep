# Indiana BMV Prep (EN / TH)

Live site: https://oke713-hash.github.io/indiana-bmv-prep/

เว็บแอปฝึกข้อสอบความรู้ Indiana BMV แบบรันบนเครื่อง สร้างด้วย React, Vite, TypeScript และ Tailwind CSS ไม่ใช้ฐานข้อมูล ข้อมูลคำถามอยู่ใน JSON และประวัติข้อผิดเก็บใน `localStorage` ของเบราว์เซอร์

## วิธีรัน

ต้องมี Node.js 18 ขึ้นไป จากนั้นเปิด Terminal ในโฟลเดอร์โปรเจกต์และรัน:

```bash
npm install
npm run dev
```

เปิด URL ที่ Vite แสดง (ปกติคือ `http://localhost:5173`)

## Build สำหรับ production

```bash
npm run build
npm run preview
```

## ข้อมูลและแหล่งอ้างอิง

- [Indiana BMV Driver’s Manual](https://www.in.gov/bmv/licenses-permits-ids/learners-permits-and-drivers-licenses-overview/drivers-manual/)
- [Indiana BMV — Learner’s Permits and Driver’s Licenses](https://www.in.gov/bmv/licenses-permits-ids/learners-permits-and-drivers-licenses-overview/)
- [Indiana BMV official website](https://www.in.gov/bmv/)

ชุดข้อมูลมี 500 รายการ ครอบคลุม Road Signs, Traffic Laws, Safe Driving และ Pavement Markings แต่ละชุดสอบ 50 ข้อจะสุ่มแบบ 13 + 13 + 12 + 12 และไม่ใช้คำถามที่มาจากข้อเท็จจริงฐานเดียวกันซ้ำในชุดเดียว เนื้อหาถูกเขียนใหม่เพื่อการฝึก ไม่ได้คัดลอกข้อสอบทางการ ควรตรวจคู่มือฉบับล่าสุดก่อนสอบจริง เพราะกฎหมายและขั้นตอนอาจเปลี่ยนได้

ภาพป้ายเป็นภาพมาตรฐาน MUTCD จากไฟล์สาธารณสมบัติของรัฐบาลสหรัฐฯ ซึ่งเผยแพร่ผ่าน Wikimedia Commons เก็บไว้ใน `public/signs/` เพื่อให้แอปทำงานออฟไลน์ ภาพเหล่านี้ไม่ใช่ตราสัญลักษณ์ของรัฐ

## โครงสร้างสำคัญ

- `src/data/questions.json` — คำถามสองภาษา ตัวเลือก เฉลย คำอธิบาย และแหล่งอ้างอิง
- `public/signs/` — ภาพป้ายจราจร
- `src/App.tsx` — หน้าจอและตรรกะการทำข้อสอบ

> แอปนี้เป็นสื่อช่วยเรียน ไม่ใช่ผลิตภัณฑ์หรือข้อสอบอย่างเป็นทางการของ Indiana BMV
