

# ใช้งาน GetMap Operation

GetMap operation ใน WMS จะถูกใช้สั่งให้ทาง GeoServer สร้างภาพแผนที่ขึ้นมาจาก paremeter ที่กำหนดให้ 

1. เปิด Web Browser
2. ใช้ URL Address ด้านล่างเข้าถึงแผนที่ 

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
```

จะพบภาพแผนที่แสดงขึ้นมา

## Workshop 

1. จากข้อมูล WMS Service ที่ได้จากขั้นตอนนี้ ให้ลองหา layer ชื่อ US Population
2. สังเกตในส่วนของ Style ว่ามี style อะไรบ้าง
3. ทดสอบแก้ไขค่า parameter ชื่อ **style** จาก URL ตัวอย่าง และสังเกตผล