
# สำรวจการทำงานของ WCS Protocol

WCS หรือ Web Coverage Service เป็นอีก Protocol หนึ่งที่นิยมใช้กับข้อมูลแบบ Raster ([สังเกตว่าแบบ WMS และ WFS จะใช้กับ Vector Data](../vector-raster-data/README.md))

- แตกต่างจาก WMS ที่ส่งรูปภาพ WCS จะส่งข้อมูลดิบกลับมาให้ Client
- ทำงานกับ Raster Data
- ไม่จำเป็นต้องเป็น GeoTiff ตราบใดที่ format ข้อมูลสามารถใช้ได้กับ Geoserver

ทดสอบเรียกใช้ WCS service ตาม URL ด้านล่างนี้ 

```
http://localhost:8080/geoserver/wcs?service=WCS&version=2.0.0&request=GetCapabilities
```

เราจะได้ XML ตอบกลับมาซึ่งก็จะมีข้อมูลที่สามารถใช้งานได้คล้ายกับที่เห็นใน WMS



