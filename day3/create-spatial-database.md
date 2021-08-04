

# การสร้าง Spatial Database

เปิดโปรแกรม pgAdmin และทำการสร้างการเชื่อมต่อไปที่ server หากยังไม่มี server ในรายการให้ทำการสร้างเพิ่มตามขั้นตอนด้านล่าง

## การสร้างการเชื่อมต่อไปที่ Server

1. จากเมนูด้านข้าง คลิกขวาที่ **Server > Create > Server...**

<img width="445" alt="2021-08-04_21-08-23" src="https://user-images.githubusercontent.com/85179/128195718-4cb968c2-aa74-4d4d-8662-a35a6ff9552e.png">


2. ใน **General** Tab ให้ตั้งชื่อ server ว่า **PostGIS**

<img width="499" alt="2021-08-04_21-09-05" src="https://user-images.githubusercontent.com/85179/128195821-1b6986f2-5184-4764-90db-205e3c939d85.png">


3. ใน **Connection** tab ให้กรอกข้อมูลดังนี้ และกดปุ่ม Save

- **host name/addesss**: localhost
- **port**: 5432
- **maintenance database**: postgres
- **username**: postgres
- **password**: ตั้งรหัสผ่าน

<img width="497" alt="2021-08-04_21-09-47" src="https://user-images.githubusercontent.com/85179/128196040-49c80754-74ef-4fb3-8904-f28532eda516.png">


## การสร้าง Spatial Database

1. จาก Server ที่เชื่อมต่ออยู่ คลิกขวาที่ **Database > Create > Database...**

<img width="480" alt="2021-08-04_21-10-56" src="https://user-images.githubusercontent.com/85179/128196330-80a0869d-fb3a-4827-8040-99e38d0e7a2c.png">


2. ใน **General** Tab กรอกข้อมูลตามนี้

- **Database**: nyc
- **Owner**: postgres

<img width="701" alt="2021-08-04_21-12-21" src="https://user-images.githubusercontent.com/85179/128196453-e42c063f-3997-4eed-b1a5-ba463745fea6.png">


## เปิดการใช้งาน

postgis เป็นส่วนเสริมที่มักติดมากับฐานข้อมูล Postgres อยู่แล้ว ในที่นี้เราจะมาเปิดใช้งานกัน

<img width="1050" alt="2021-08-04_21-13-47" src="https://user-images.githubusercontent.com/85179/128196794-fc982778-a33b-47f2-ad4a-5021d8cfe2fd.png">


1. เลือก nyc database จากเมนูด้านข้าง 
2. คลิกปุ่ม **Query Tool** 
3. เขียนคำสั่งด้านล่าง เพื่อโหลด postgis extension มาใช้งาน

```sql
CREATE EXTENSION postgis;
```

4. กดปุ่ม Play (หรือ F5)
5. รันคำสั่งด้านล่างเพื่อทดสอบว่า PostGIS ทำงานใน Database นี้แล้ว

```sql
SELECT postgis_full_version();
```

6. จะเห็นส่วนของข้อมูล extension แสดงขึ้นมา
