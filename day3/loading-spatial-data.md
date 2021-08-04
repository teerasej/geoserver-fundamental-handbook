
# การโหลด Spatial Data

สามารถดาวน์โหลดไฟล์ที่ใช้ใน workshop นี้[ได้จากที่นี่](https://www.dropbox.com/s/ejnppxj6bfvpl5l/nyc_data.backup.zip?dl=0)

## โหลดข้อมูลจาก Backup 

1. จากเมนูด้านซ้ายมือ คลิกขวาที่ฐานข้อมูล **nyc > Restore...**

<img width="344" alt="2021-08-04_21-25-39" src="https://user-images.githubusercontent.com/85179/128198639-8f3b9341-58b0-440c-93c0-20238fe292f1.png">


2. จากโฟลเดอร์ข้อมูลสำหรับทำ workshop ให้เลือกไฟล์ชื่อ **nyc_data.backup**

<img width="698" alt="2021-08-04_21-26-54" src="https://user-images.githubusercontent.com/85179/128199119-26872620-6f55-4ce7-be7a-a943a51dd7d7.png">


3. ในส่วน **restore options** tab **> do not save** ให้เลือก **owner** เป็น yes
จากนั้นกดปุ่ม **Restore**

<img width="700" alt="2021-08-04_21-27-13" src="https://user-images.githubusercontent.com/85179/128199136-6c609938-dae8-4e78-9fd4-540ab2a4046d.png">


4. หลังจากการ restore เสร็จสมบูรณ์ ให้คลิกขวาที่ฐานข้อมูล **nyc > Refresh...**
5. ให้สำรวจดู table ในฐานข้อมูล nyc โดยคลิกดูตามลำดับ

**nyc > Schemas > public > Tables**

จะเห็นว่ามี Table ข้อมูลต่างๆ อยู่ด้านใน

<img width="314" alt="2021-08-04_21-28-09" src="https://user-images.githubusercontent.com/85179/128199220-abb0b962-5834-4604-a1e7-d05778e280ca.png">


- **spatial_ref_sys** table เป็น table มาตรฐานที่มีข้อมูลการอ้างอิงทางภูมิศาสตร์ต่างๆ ให้ฐานข้อมูล ซึ่งมีมากกว่า 3000 ระบบ 


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
