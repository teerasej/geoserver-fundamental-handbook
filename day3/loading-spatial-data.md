
# การโหลด Spatial Data

สามารถดาวน์โหลดไฟล์ที่ใช้ใน workshop นี้[ได้จากที่นี่](https://www.dropbox.com/s/ejnppxj6bfvpl5l/nyc_data.backup.zip?dl=0)

## โหลดข้อมูลจาก Backup 

จากเมนูด้านซ้ายมือ คลิกขวาที่ฐานข้อมูล **nyc > Restore...**



จากโฟลเดอร์ข้อมูลสำหรับทำ workshop ให้เลือกไฟล์ชื่อ **nyc_data.backup**


ในส่วน **restore options** tab **> do not save** ให้เลือก **owner** เป็น yes
จากนั้นกดปุ่ม **Restore**



หลังจากการ restore เสร็จสมบูรณ์ ให้คลิกขวาที่ฐานข้อมูล **nyc > Refresh...**

ให้สำรวจดู table ในฐานข้อมูล nyc โดยคลิกดูตามลำดับ

**nyc > Schemas > public > Tables**

จะเห็นว่ามี Table ข้อมูล

## อื่นๆ 

นอกจากการใช้ไฟล์ backup ในการโหลดข้อมูลเข้า PostGIS Database แล้ว ยังมีเครื่องมือขั้นสูงที่สามารถนำมาใช้งานกับ PostGIS Table ได้

1. [ogr2ogr](https://postgis.net/workshops/postgis-intro/loading_data.html#loading-with-ogr2ogr) 
- Command line 
- ใช้สั่งแปลงข้อมูลระหว่า GIS Data format, file format ทั่วไป และฐานข้อมูล spatial database
- ทำงานกับ Database โดยตรง

2. [shp2pgsql](https://postgis.net/workshops/postgis-intro/loading_data.html#loading-with-shp2pgsql)
- Command line
- แปลง Shape file เป็น SQL
- ปกติมักติดมากับ PostgreSQL
- ไม่เหมือนกับ ogr2ogr เจ้านี่แปลง shape file เป็น sql อย่างเดียว ไม่ยิงเข้า database

3. [SRID 26918](https://postgis.net/workshops/postgis-intro/loading_data.html#srid-26918-what-s-with-that)

- เครื่องมือขั้นสูงสุดมักใช้โดย ผู้เชี่ยวชาญ GIS โดยเฉพาะ
