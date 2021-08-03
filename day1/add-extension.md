
# การใช้งาน Extension 

ระบบ GeoServer มีความสามารถในการเพิ่มเติมส่วนเสริม หรือที่เรียกว่า Extension ได้ โดย Extension จะแบ่งออกเป็น 3 กลุ่ม

- **Core** ส่วนการทำงานหลัก และมักติดมากับตัว GeoServer เลย
- **Extension** เป็นส่วนการทำงานหลักเหมือนกัน แต่เป็นเหมือนตัวเลือกเสริม เลยแยกออกมาจากตัวหลัก ให้ติดตั้งเอง [ดูได้จากหน้าดาวน์โหลด GeoServer](http://geoserver.org/release/stable/) 
- **Community** อันนี้ชุมชนร่วมด้วยช่วยกัน เป็นพวก 3rd-party

** ให้แน่ใจว่าเวอร์ชั่นของ plugin ตรงกับเวอร์ชั่นของ Geoserver

## การติดตั้ง Extension 

ในที่นี้เราจะมีการติดตั้ง Extension CSS เพื่อใช้ในส่วนของการทำ Styling Map 

1. [ดาวน์โหลดไฟล์ **geoserver-X.XX-SNAPSHOT-css-plugin.zip**](https://www.dropbox.com/s/tjm6q60zs7x15ez/geoserver-2.19.2-css-plugin.zip?dl=0)
2. แตก zip จะเห็นว่ามีไฟล์ jar จำนวนหนึ่งอยู่ในโฟลเดอร์
3. copy ไฟล์ jar ไปไว้ใน `{geoserver directory}/webapps/geoserver/WEB-INF/lib`
4. รีสตาร์ท geoserver 