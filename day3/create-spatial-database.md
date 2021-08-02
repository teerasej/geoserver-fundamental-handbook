

# การสร้าง Spatial Database



เปิดโปรแกรม pgAdmin และทำการสร้างการเชื่อมต่อไปที่ server หากยังไม่มี server ในรายการให้ทำการสร้างเพิ่มตามขั้นตอนด้านล่าง

## การสร้างการเชื่อมต่อไปที่ Server

1. จากเมนูด้านข้าง คลิกขวาที่ Server > Create > Server...

![](https://postgis.net/workshops/postgis-intro/_images/pgadmin_01.png)

2. ใน General Tab ให้ตั้งชื่อ server ว่า PostGIS



3. ใน Connection tab ให้กรอกข้อมูลดังนี้

- host name/addesss: localhost
- port: 5432
- maintenance database: postgres
- username: postgres
- password: ตั้งรหัสผ่าน

## การสร้าง Spatial Database

1. จาก Server ที่เชื่อมต่ออยู่ คลิกขวาที่ Database > Create > Database...
2. ใน General Tab กรอกข้อมูลตามนี้

- Database: nyc
- Owner: postgres

## เปิดการใช้งาน

postgis เป็นส่วนเสริมที่มักติดมากับฐานข้อมูล Postgres อยู่แล้ว ในที่นี้เราจะมาเปิดใช้งานกัน

1. จากเมนูด้านข้าง คลิกปุ่ม Query Tool 
2. เขียนคำสั่งด้านล่าง เพื่อโหลด postgis extension มาใช้งาน

```sql
CREATE EXTENSION postgis;
```

3. กดปุ่ม Play (หรือ F5)
4. รันคำสั่งด้านล่างเพื่อทดสอบว่า PostGIS ทำงานใน Database นี้แล้ว

```sql
SELECT postgis_full_version();
```