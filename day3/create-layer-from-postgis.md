
# สร้าง Store และ layer จาก PostGIS

## สร้าง PostGIS Store

1. login เข้าใช้งาน GeoServer 
2. ถ้ายังไม่มี workspace ให้สร้าง และตั้งชื่อว่า nextflow
3. จากเมนู **Data > Store** ให้เลือก **Add New Store**
4. เลือกแบบ **PostGIS**
5. กรอกข้อมูลตามด้านล่าง 

- **Data Source Name**: nyc_building
- **host**: localhost
- **port**: 5432
- **database**: nyc
- **schema**: public
- **user**: postgres (หรือที่ตั้งไว้ตอนสร้างฐานข้อมูล)
- **passwd**: ที่ตั้งไว้ตอนสร้างฐานข้อมูล

6. กดปุ่ม **Save** 

## สร้าง Layer

1. หลังจากสร้าง PostGIS Store แล้ว GeoServer จะเสนอการสร้าง Layer โดยอิงกับ Table ในฐานข้อมูล
2. ให้กด publish **nyc_neighborhoods**
3. ทำการกำหนดข้อมูลตามด้านล่าง 

- **Name**: nyc_neighborhoods
- **Title**: NYC neighborhoods
- **Bounding Boxes**: กด Compute from Data, และ Compute from Native bounds ตามลำดับ

4. สังเกตในส่วน **Feature Type Details** ว่ามี 3 Property 
5. กด **Save**


