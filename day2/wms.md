
# Web Map Service

หนึ่งใน Service สำคัญของ GeoServer มักถูกเรียกใช้ในการนำเสนอข้อมูลแผนที่

1. [ดูตัวอย่างของข้อมูล Web Map Service ผ่าน GeoServer](wms-geoserver-example.md)
2. [ทดสอบดูรายละเอียดของ WMS Service ผ่าน Web Browser](wms-access-service-via-webbrowser.md)

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