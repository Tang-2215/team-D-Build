# อ่านก่อน
---
### วิธีใช้งาน
1. **ติดตั้งครั้งแรกใช้ git clone https://github.com/Tang-2215/team-D-Build.git**
    - ใช้งานตามปกติไม่ต้อง git pull
    - git add . / git add "file"
    - git commit -m "ข้อความบันทึก" = (อัพเดทอะไรเข้ามาแจ้งด้วย)
    - git push = อัพเดทจากเครื่องเราเข้า git hub

2. **ถ้าลงมานานแล้วให้**
    - git pull = อัพเดทงานจาก git hub มาลงที่เครื่องก่อยกรณี มีเพื่อนอัพเดทมาก่อนเรา **(ทุกครั้งก่อนจะอัพเดท)**
    - git add . / git add "file"
    - git commit -m "ข้อความบันทึก" = (อัพเดทอะไรเข้ามาแจ้งด้วย)
    - git push = อัพเดทจากเครื่องเราเข้า git hub

---

# คำสั่ง Git ที่ใช้บ่อย

## 1. เริ่มต้นและตั้งค่า

git init  
สร้าง Git repository ใหม่ในโฟลเดอร์ปัจจุบัน  

git clone <URL>  
ก๊อปปี้ repository จาก GitHub มายังเครื่องเรา  

git config --global user.name "ชื่อของคุณ"  
ตั้งชื่อผู้ใช้ที่จะบันทึกใน commit  

git config --global user.email "อีเมลของคุณ"  
ตั้งอีเมลผู้ใช้ที่จะบันทึกใน commit  

---

## 2. ตรวจสอบสถานะ

git status  
ดูไฟล์ที่แก้ไขแล้ว, ไฟล์ที่ยังไม่ถูก track, และสถานะ staging  

git log  
ดูประวัติ commit  

git diff  
ดูความต่างของไฟล์ที่ยังไม่ได้ staging  

---

## 3. เพิ่มและบันทึกการเปลี่ยนแปลง

git add <ไฟล์>  
เพิ่มไฟล์เข้า staging area (เตรียม commit)  

git add .  
เพิ่มทุกไฟล์ที่แก้ไขทั้งหมด  

git commit -m "ข้อความบันทึก"  
ทำการ commit การเปลี่ยนแปลงพร้อมใส่ข้อความอธิบาย  

---

## 4. ทำงานกับ branch

git branch  
แสดง branch ที่มีอยู่  

git branch <ชื่อ branch>  
สร้าง branch ใหม่  

git checkout <ชื่อ branch>  
สลับไปยัง branch นั้น  

git checkout -b <ชื่อ branch>  
สร้าง branch ใหม่และสลับไปเลย  

git merge <ชื่อ branch>  
รวมการเปลี่ยนแปลงจาก branch อื่นเข้ามาใน branch ปัจจุบัน  

---

## 5. ทำงานกับ remote (GitHub)

git remote add origin <URL>  
ผูก repository ในเครื่องเข้ากับ GitHub  

git push -u origin main  
อัปโหลด branch main ขึ้น GitHub ครั้งแรก  

git push  
อัปโหลด commit ล่าสุดขึ้น GitHub  

git pull  
ดึงการเปลี่ยนแปลงล่าสุดจาก GitHub มาที่เครื่อง  

git fetch  
ดึงข้อมูลการเปลี่ยนแปลง (แต่ยังไม่ merge เข้ามา)  

---

## 6. ยกเลิกหรือย้อนกลับ

git checkout -- <ไฟล์>  
ยกเลิกการแก้ไขไฟล์ที่ยังไม่ได้ staging  

git reset HEAD <ไฟล์>  
เอาไฟล์ออกจาก staging area แต่ไม่ลบการแก้ไข  

git revert <commit>  
ย้อนกลับ commit ใด commit หนึ่ง โดยสร้าง commit ใหม่  

git reset --hard <commit>  
ย้อน repository กลับไปที่ commit ใด commit หนึ่ง (ลบการเปลี่ยนแปลงทั้งหมดหลัง commit นั้น — อันตราย!)  
