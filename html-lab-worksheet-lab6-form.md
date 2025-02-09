# ใบงานการทดลอง HTML

## การทดลองที่ 6: การสร้างฟอร์ม
### วัตถุประสงค์
- สร้างฟอร์มรับข้อมูลได้ตามกำหนด
- เลือกใช้ประเภทของ input แบบต่างๆ ได้เหมาะสม
- สามารถใช้งาน form validation ได้

### ขั้นตอนการทดลอง
1. สร้างฟอร์มลงทะเบียนนักศึกษา:
```html

```

### คำอธิบายเพิ่มเติม
1. Input Types ที่ใช้:
   - text: สำหรับข้อความทั่วไป
   - email: สำหรับอีเมล (มีการตรวจสอบรูปแบบอัตโนมัติ)
   - tel: สำหรับเบอร์โทรศัพท์
   - date: สำหรับวันที่
   - number: สำหรับตัวเลข
   - radio: สำหรับตัวเลือกเดียว
   - checkbox: สำหรับหลายตัวเลือก
   - file: สำหรับอัพโหลดไฟล์
   - select: สำหรับรายการแบบเลือก
   - textarea: สำหรับข้อความหลายบรรทัด

2. Attributes ที่สำคัญ:
   - required: จำเป็นต้องกรอก
   - pattern: กำหนดรูปแบบข้อมูล
   - min/max: กำหนดค่าต่ำสุด/สูงสุด
   - accept: กำหนดประเภทไฟล์ที่ยอมรับ
   - multiple: เลือกได้หลายตัวเลือก

### แบบฝึกหัด
1. สร้างฟอร์มสมัครสมาชิกร้านค้าออนไลน์ที่มี:
   - ข้อมูลส่วนตัว (ชื่อ-นามสกุล, วันเกิด, เพศ)
   - ข้อมูลการติดต่อ (อีเมล, เบอร์โทร, ที่อยู่จัดส่ง)
   - รูปโปรไฟล์
   - การยืนยันรหัสผ่าน
   - ความสนใจในหมวดหมู่สินค้า
   - การยอมรับเงื่อนไขการใช้งาน

2. เพิ่ม validation ที่เหมาะสม:
   - ตรวจสอบรูปแบบอีเมล
   - ตรวจสอบความยาวรหัสผ่าน
   - ตรวจสอบรูปแบบเบอร์โทร
   - ตรวจสอบขนาดไฟล์รูปภาพ

### บันทึกผลการทดลอง
[วางโค้ด HTML ที่นี่]
```
<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>สมัครสมาชิกร้านค้า</title>
</head>
<body>
    <h1>สมัครสมาชิกร้านค้าข</h1>
    <form action="/submit-form" method="POST" enctype="multipart/form-data">
        <label for="fullname">ชื่อ-นามสกุล:</label>
        <input type="text" id="fullname" name="fullname" required><br>

        <label for="birthdate">วันเกิด:</label>
        <input type="date" id="birthdate" name="birthdate" required><br>

        <label for="gender">เพศ:</label>
        <select id="gender" name="gender">
            <option value="male">ชาย</option>
            <option value="female">หญิง</option>
            <option value="other">อื่น ๆ</option>
        </select><br>

        <label for="email">อีเมล:</label>
        <input type="email" id="email" name="email" required><br>

        <label for="phone">เบอร์โทร:</label>
        <input type="tel" id="phone" name="phone" pattern="[0-9]{10}" required><br>

        <label for="address">ที่อยู่จัดส่ง:</label>
        <textarea id="address" name="address" required></textarea><br>

        <label for="profilePicture">รูปโปรไฟล์:</label>
        <input type="file" id="profilePicture" name="profilePicture" accept="image/*" required><br>


        <label for="password">รหัสผ่าน:</label>
        <input type="password" id="password" name="password" minlength="8" required><br>

        <label for="confirmPassword">ยืนยันรหัสผ่าน:</label>
        <input type="password" id="confirmPassword" name="confirmPassword" minlength="8" required><br>


        <label>ความสนใจในหมวดหมู่สินค้า:</label><br>
        <input type="checkbox" id="electronics" name="interests" value="electronics">
        <label for="electronics">Pc Computer</label><br>

        <input type="checkbox" id="clothing" name="interests" value="clothing">
        <label for="clothing">Gaming Gear</label><br>

        <input type="checkbox" id="beauty" name="interests" value="beauty">
        <label for="beauty">mobile phone</label><br>


        <input type="checkbox" id="terms" name="terms" required>
        <label for="terms">ฉันยอมรับเงื่อนไขการใช้งาน</label><br>

        <input type="submit" value="สมัครสมาชิก">
    </form>
</body>
</html>
```
- ภาพผลลัพธ์:
[วางภาพ screenshot ที่นี่]
![lab 6](https://github.com/user-attachments/assets/3cffb242-0097-4e79-8792-57c7d5508987)



