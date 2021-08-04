

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

## Workshop 1

1. จากข้อมูล WMS Service ที่ได้จากขั้นตอนนี้ ให้ลองหา layer ชื่อ **US Population**
2. สังเกตในส่วนของ **Style** ว่ามี style อะไรบ้าง
3. ทดสอบแก้ไขค่า parameter ชื่อ **style** จาก URL ตัวอย่าง และสังเกตผล


## Workshop 2

จาก Request URL ด้านล่างให้ลองปรับเป็น Layer ชื่อ tiger:poly_landmarks ทีละขั้นตอนและสังเกตผล

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
```

1. กำหนด Layers เป็น **tiger:poly_landmarks** (tiger%3Apoly_landmarks)

ส่วนนี้จะได้ XML Error กลับมาเป็น 

```xml
<?xml version="1.0" encoding="UTF-8" standalone="no"?><!DOCTYPE ServiceExceptionReport SYSTEM "http://localhost:8080/geoserver/schemas/wms/1.1.1/WMS_exception_1_1_1.dtd"> <ServiceExceptionReport version="1.1.1" >   <ServiceException>
      The requested Style can not be used with this layer.  The style specifies an attribute named &apos;STATE_ABBR&apos;, not found in the &apos;tiger:poly_landmarks&apos; layer
</ServiceException></ServiceExceptionReport>
```

เพราะในที่นี้ Style มีการใช้ Attribute `STATE_ABBR` ซึ่งไม่มีข้อมูลนี้ใน **tiger:poly_landmarks** layer

2. ลบ `&styles=population` ออก และทดสอบอีกครั้ง คราวนี้จะแสดงผลได้ แต่จะอยู่ไกลจากแผนที่หน่อยต้องซูมดีๆ 

เพราะในที่นี้ bounding boxes ของ **topp:states** layer เป็นคนละแบบกับ **tiger:poly_landmarks** layer

3. ดังนั้นให้ลองเปิดไปดูรายละเอียดของ **tiger:poly_landmarks** layer และเอาพิกัดของ native bounding boxes มาแทนในส่วนของ `&bbox=...`

จะได้ผลแบบด้านล่าง

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

## Workshop 3 Reflector

ในกรณีที่เราส่ง request เราสามารถใช้ [Reflector](https://docs.geoserver.org/stable/en/user/tutorials/wmsreflector.html) ในการใช้งาน เพื่อลดความซับซ้อนของ Request URL ได้ เช่น

```
http://localhost:8080/geoserver/wms/reflect?layers=topp:states
```

```
// Layer groups
http://localhost:8080/geoserver/wms/reflect?layers=spearfish
```

และยังสามารถทำไปใช้ใน Web Client ได้เช่นเดียวกัน 

```html
<img src="http://localhost:8080/geoserver/wms/reflect?layers=topp:states&width=400" />
```
