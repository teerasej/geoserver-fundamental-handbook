# Workshop โหลดไฟล์เข้า GeoServer ผ่าน data directory

## 1. เตรียมไฟล์

1. [ดาวน์โหลดไฟล์ zip](https://docs.geoserver.org/latest/en/user/_downloads/30e405b790e068c43354367cb08e71bc/nyc_roads.zip)
2. แตก zip ไฟล์ จะได้ directory ชื่อ **nyc_roads** ด้านในจะมีไฟล์ทั้งหมด 4 ไฟล์ นี่นับเป็น 1 shape file
3. นำ directory **nyc_roads** ไปไว้ใน **data_dir/data** ของ GeoServer

## 2. สร้าง Workspace

1. [Login เข้าใช้งาน GeoServer](login-admin-firsttime.md)
2. จากเมนูด้านข้างซ้าย เลือก Data > Workspaces
3. กดเลือก **Add new workspace**
4. กรอกข้อมูล และกดปุ่ม **submit**

- **Name**: nyc
- **Namespace** URI: http://nextflow.in.th/nyc

## 3. สร้าง Store

1. จากเมนูด้านข้างซ้าย เลือก **Data > Stores**
2. กดเลือก **Add new store**
3. เลือก **Vector Data Source > Shapefile**
4. กำหนดข้อมูล 

- **Workspace**: nyc
- **Data Source Name**: NYC Roads
- **Description**: ถนนเมืองนิวยอร์คซีตี้
- **Connection** Parameters > Shapefile locations > กดปุ่ม Browse ไฟล์ที่อยู่ใน Data directory

5. กดปุ่ม **Save** หลังจากนี้เราจะถูกพาไปยังหน้า New Layer อัตโนมัติ

### สร้าง Layer

6. ชื่อ Layer จะถูกตั้งตามไฟล์คือ **nyc_roads**
7. กด **publish**
8. หน้า edit layer ให้แก้ไขข้อมูลตามนี้

- **Name**: nyc_roads
- **Title**: Subset of NYC Roads
- **Abstract**: Shapefile of NYC Roads

9. เลื่อนลงมาด้านล่างในส่วน **Bounding Boxes** 
10. ให้กด **Compute from data** และ **Compute from native bounds** เพื่อให้ GeoServer ตั้งค่าจากข้อมูลของ Shapefile
11. เลื่อนขึ้นมาด้านบน และกดเข้าไปที่ **Publishing tab**
12. ลงมาที่ **WMS Setting** และเลือก **Default style** เป็น **line**

### Preview 

1. จากเมนูด้านข้าง เลือก **Layer Preview**
2. ค้นหา **nyc_roads**
3. จากส่วน Common Format ให้เลือก **Open Layer**

ทดสอบกลับไปเปลี่ยน **Default Style** เป็น **Polygon** และทดสอบ Preview Layer อีกครั้ง