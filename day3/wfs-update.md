
# การใช้งาน WFS Feature ในการแก้ไขอัพเดตข้อมูลบน Layer

WFS มีความสามารถในการอัพเดตการแก้ไขข้อมูลจากฝั่ง client ด้วย ทำให้เราสามารถสร้าง client ที่มีคุณสมบัติอัพเดตข้อมูลของ feature ได้

## ทดสอบการแก้ไข

1. เปิดแอพ QGIS
2. เชื่อมต่อไปที่ GeoServer แต่คราวนี้ให้เชื่อมต่อแบบ WFS
3. ใช้ข้อมูลตามด้านล่าง 

- **Name**: Tasmania WFS
- **URL**: http://localhost:8080/geoserver/topp/wfs
- **Authentication** > **Basic**
  - **Username**: admin
  - **Password**: รหัสผ่านที่ตั้งไว้

4. กดปุ่ม **Connect**
5. เลือก Layer **USA Population** มาใส่ในโปรเจค

### แก้ไขค่า Feature ด้วย Attribute Table

1. คลิกขวาที่ Layer **USA Population**
2. เลือก **Open Attribute Table**
3. คลิก **Toggle Edit Mode**
4. ทำการแก้ไขข้อมูลของรัฐ Arizona
5. คลิกขวาที่ Layer และเลือก **Save Layer Edit**

### แสดงผลการแก้ไข

6. คลิกขวาที่ Layer และเลือก **Properties**
7. ในส่วนของ Label ให้เลือกแสดง STATE_NAME
8. สังเกตข้อมูลของรัฐ Arizona 

### แสดงผลการแก้ไขบน GeoServer

9. Login เข้าใช้งาน GeoServer
10. จากเมนูด้านซ้าย ไปที่ Data > Layer Preview
11. เลือกพรีวิว USA Population 
12. สังเกตการเปลี่ยนแปลง



## Exercise: Edit Main Road

Exercise นี้จำเป็นต้องมีการ[สร้าง Main Road Layer](../day1/exercise-publish-shapfile.md) ไว้แล้ว

1. ให้ทดลองเปิด Main Road Layer ผ่าน WFS Service ด้วยข้อมูลต่อไปนี้ 

- **Name**: Nextflow WFS
- **URL**: http://localhost:8080/geoserver/Nextflow/wfs
- **Authentication** > **Basic**
  - **Username**: admin
  - **Password**: รหัสผ่านที่ตั้งไว้

2. ทำการ import Layer Main Road มาแสดงใน QGIS
3. ทดลองใช้ Editing Mode แก้ไขถนนบน Layer
4. บันทึกการแก้ไข
5. ทดสอบพรีวิว Layer Main Road ผ่าน GeoServer