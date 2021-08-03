
# การ Publish Raster Data แบบรวมภาพถ่ายมุมสูง (Image Mosaic)

Raster Data อีกรูปแบบมักมาในแบบภาพถ่ายทางอากาศ หรือภาพถ่ายจากดาวเทียมที่มีการถ่ายภาพเป็น shot ครอบคลุมพื้นที่ขนาดใหญ่ 

1. คัดลอก directory ชื่อ **aerial** จาก **raster_data** มาไว้ใน **data_dir/data**
2. สำรวจไฟล์รูปภาพด้านใน จะเห็นว่าเป็นภาพถ่ายทางอากาศหลายๆ ภาพ
3. [Login เข้าใช้งาน Geoserver](../../day1/login-admin-firsttime.md)
4. เลือกสร้าง Store ใหม่
5. เลือก **Raster Data Source > Image Mosaic**
6. ตั้งชื่อ **Data source name** เป็น **boulder_bg**
7. ส่วนของ **Connection Parameters** ให้กด **browse** และเลือก directory **aerial**
8. ในส่วนของ New Layer ให้กด Publish
9. เปลี่ยนชื่อ Layer เป็น **boulder_bg**
10. สังเกตส่วนของ **Coordinate Reference Systems** และ **Bounding Boxes** ว่ามีค่าที่ Geoserver คำนวนจากข้อมูลภาพทั้งหมดใส่ไว้ให้แล้ว
11. กดปุ่ม Save
12. ทดสอบ Layer Preview จะเห็นว่า Geoserver นำภาพถ่ายทางอากาศทั้งหมดมารวมเป็นภาพเดียว