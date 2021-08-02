
# ทดสอบดูรายละเอียดของ WMS Service ผ่าน Web Browser

1. เปิด Web Browser 
2. ใส่ข้อมูลดังต่อไปนี้ ลงไปใน Address bar และกด enter

```
http://localhost:8080/geoserver/wms?
service=wms&
version=1.1.1&
request=GetCapabilities
```

3. สังเกตว่าเราจะได้ไฟล์​ XML มาไฟล์หนึ่ง ซึ่งจะประกอบไปด้วย 3 ส่วน

    1. **Service** รายละเอียดของ Services เช่นชื่อ keyword หรือข้อมูลผู้ให้บริการ Service
    2. **Request** รายการ operation ต่างๆ รวมถึง parameters และ output format ของแต่ละ Operation
    3. **Layer** รายชื่อ Layer และ Coordinate system ต่างๆ 
