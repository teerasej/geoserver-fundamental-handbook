
# การ Filter ข้อมูล

WMS แบบมาตรฐานมักเปิดให้มีการ Query ข้อมูลจาก Layer ได้ (เรียกว่าการทำ filter)

การทำ filter มี 3 วิธี
- CQL
- OGC
- Feature ID

## การใช้ OpenLayer ทดสอบการปรับ Filter 

1. ลงชื่อเข้าใช้ GeoServer
2. เข้าไปที่ Data > Layer Preview
3. ค้นหา Layer ชื่อ **USA Population**
4. เลือก Common Formats เป็น **OpenLayers**

จากส่วนนี้กดปุ่ม ... เพื่อเปิด Tool bar ขึ้นมา

toolbar พวกนี้คือ Parameter ที่สามารถส่งมาพร้อมกับ request ได้ 

## ทดสอบปรับค่า parameter ใน Toolbar

1. ค่า Tiling 
   1. ซูมแผนที่เข้าไปในระดับรัฐ
   2. ทดสอบปรับ tiling จาก single เป็น tiled
2. ค่า antilias
3. ค่า Format ที่ทำให้ได้รูปที่แตกต่างกัน
4. ค่า Style

## การใช้งาน filter 

