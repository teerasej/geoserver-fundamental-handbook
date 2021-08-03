
# การ Filter ข้อมูล

WMS แบบมาตรฐานมักเปิดให้มีการ Query ข้อมูลจาก Layer ได้ (เรียกว่าการทำ filter)

การทำ filter มี 3 วิธี

- CQL
- OGC
- Feature ID

## การใช้ OpenLayer ทดสอบการปรับ Filter 

1. [ลงชื่อเข้าใช้ GeoServer](../day1/login-admin-firsttime.md)
2. เข้าไปที่ **Data > Layer Preview**
3. ค้นหา Layer ชื่อ **USA Population**
4. เลือก Common Formats เป็น **OpenLayers**

จากส่วนนี้กดปุ่ม **...** เพื่อเปิด Tool bar ขึ้นมา เครื่องมือที่เห็นคือ Parameter ที่สามารถส่งมาพร้อมกับ request ได้ 

<img width="959" alt="2021-08-03_21-23-30" src="https://user-images.githubusercontent.com/85179/128032630-e63b9c95-82a8-455e-a862-1f9e13885361.png">


## ทดสอบปรับค่า parameter ใน Toolbar

5. ค่า Tiling 
   - ซูมแผนที่เข้าไปในระดับรัฐ
   - ทดสอบปรับ tiling จาก single เป็น tiled
6. ค่า antilias
7. ค่า Format ที่ทำให้ได้รูปที่แตกต่างกัน
8. ค่า Style

## การใช้งาน filter 

9. ทดสอบคลิกรัฐ Texus บนแผนที่ จะเห็น attribute ถูกแสดงขึ้นมาด้านล่าง
10. ในส่วนของ filter เลือก CQL
11. ทดสอบใส่ CQL ตามลำดับด้านล่าง และกด apply
    - PERSONS>5000000
    - LAND_KM<200000

12. ทดสอบนำ cql เข้าไปใน [URL ตัวอย่างของ GetMap](wms-getmap-operation.md) และเปิดผ่านหน้าเว็บ

```
http://localhost:8080/geoserver/wms?
request=GetMap
&service=WMS
&version=1.1.1
&layers=topp%3Astates
&styles=population
&srs=EPSG%3A4326
&bbox=-145.15104058007,21.731919794922,-57.154894212888,58.961058642578&
&width=780
&height=330
&format=image%2Fpng
&CQL_FILTER=LAND_KM<200000
```

ตัวอย่างการเปิดแบบ openlayer

```
http://localhost:8080/geoserver/wms?
request=GetMap
&service=WMS
&version=1.1.1
&layers=topp%3Astates
&styles=population
&srs=EPSG%3A4326
&bbox=-145.15104058007,21.731919794922,-57.154894212888,58.961058642578&
&width=780
&height=330
&format=application%2Fopenlayers
&CQL_FILTER=LAND_KM<200000
```

## ทดสอบ

```
http://localhost:8080/geoserver/wms?
request=GetMap
&service=WMS
&version=1.1.1
&layers=tiger%3Apoly_landmarks
&srs=EPSG%3A4326
&bbox=-74.047185,40.679648,-73.90782,40.882078&
&width=780
&height=330
&format=application%2Fopenlayers
```
