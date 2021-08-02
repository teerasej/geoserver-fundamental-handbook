

# การอ้างอิง และจัดการไฟล์ด้วย Data Directory

ข้อมูลส่วนหนึ่งที่มีการใช้งานมาช้านานบน GeoServer คือข้อมูลประเภทไฟล์ ซึ่ง Geoserver ก็ได้สร้างสิ่งที่เรียกว่า data directory ขึ้นมาเพื่อจัดการไฟล์ข้อมูลพวกนี้โดยเฉพาะ 

การทำ Workshop ส่วนนี้ได้ [จะต้อง Login เข้าใช้งานก่อน](login-admin-firsttime.md)

## ที่อยู่ของ Data Directory 

1. เปิดมาที่ directory geoserver ในระบบ
2. จะเห็น directory ชื่อ **data_dir** 
3. ด้านในโฟลเดอร์นี้จะมีโฟลเดอร์ชื่อ **data** ด้วย
4. ที่นี่เป็นที่ๆ เราสามารถนำ shape file มาใส่เพื่อโหลดเข้า Geoserver ต่อไปได้อีก

นอกเหนือจากนั้น ลองสำรวจ directory ที่อยู่ใน **data_dir** 

- **layergroups** รวมไฟล์ xml ที่ระบุข้อมูลของ layer groups
- **styles** รวมไฟล์ sld และ xml ของ Style แบบต่างๆ  

