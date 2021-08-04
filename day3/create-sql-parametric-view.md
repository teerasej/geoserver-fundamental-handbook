
# การสร้าง SQL Parametric View based Layer

- ต้องทำการสร้าง Store จาก PostGIS Database [ใน workshop นี้แล้ว](create-layer-from-postgis.md)

## เริ่มต้นสร้าง SQL Parametric View

1. [login เข้าใช้งาน GeoServer](../day1/login-admin-firsttime.md)
2. จากเมนูด้านซ้าย เลือก **Data > Layers**
3. กด **Add a new layer**
4. เลือก Store เป็น **Nextflow:nyc_buildings**
5. ในส่วนนี้ แทนที่จะ publish ตาม layer ที่ให้มาโดยตรง ให้เลือก **Configure new SQL view...**
 
<img width="688" alt="2021-08-04_22-01-22" src="https://user-images.githubusercontent.com/85179/128206639-fcd3557d-405b-411d-b1df-670b19584d84.png">

## การระบุข้อมูลใน SQL view

1. กำหนดชื่อ View
2. เขียน SQL Query ลงในช่อง SQL Statement
3. กำหนดส่วนของ Attibute ที่จะนำมาใช้ใน Layer

<img width="691" alt="2021-08-04_22-06-28" src="https://user-images.githubusercontent.com/85179/128206800-58bd9692-e2ee-4eeb-a6d3-3a6d16e2ffec.png">

## การใช้งาน Attribute Table 

โดยปกติ GeoServer จะพยายามดึง Attribute ที่ได้จาก SQL statement มาแสดง โดยการกดปุ่ม refresh 
โดยเฉพาะในส่วน Geometry ที่ทาง GeoServer จะพยายามกำหนด type และ SRID แต่ก็ควรเช็คทุกครั้ง ว่าถูกต้องตามที่ควรจะเป็นหรือไม่

<img width="704" alt="2021-08-04_22-05-54" src="https://user-images.githubusercontent.com/85179/128206818-fa563c3f-c56a-4b7a-b802-93a2d8bbcf77.png">

เสร็จแล้วกด Save จะเป็นการสร้าง Layer ใหม่ (ซึ่งเราจะไม่สามารถกลับมาแก้ไข SQL View ได้อีก
