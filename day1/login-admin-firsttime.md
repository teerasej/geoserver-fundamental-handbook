
# สำรวจส่วนผู้ดูแลระบบ 1

1. เปิดมาที่ [http://localhost:8080/geoserver](http://localhost:8080/geoserver)
2. สำรวจเมนูทางด้านซ้าย จะเห็นแค่ส่วน Layer Preview
3. ใช้ข้อมูลด้านล่าง login เข้าใช้งาน

Username: admin
Password: geoserver

4. หลังจาก Login แล้ว ให้สังเกตเมนูด้านซ้าย

    - **ส่วน Server Status**
      - **Status** สถานะการทำงานของระบบ
      - **Module** ที่ติดตั้งอยู่ใน geoserver
      - **System** Status สถานะของเครื่องที่ geoserver เปิดใช้งานอยู่
    - **ส่วน GeoServer Logs** แสดง Logs การทำงาน
    - **ส่วน Contact Information** ข้อมูลของผู้ให้บริการ GeoServer ข้อมูลนี้จะติดไปกับ Response ที่ส่งให้ client ด้วย

## เปลี่ยน Master Password 

ส่วนที่จำเป็นต้องทำใน Production เราสามารถเปลี่ยน Master Password ได้ทันทีหลังล๊อคอินเข้ามาแล้ว

<img width="573" alt="2021-08-02_11-41-16" src="https://user-images.githubusercontent.com/85179/127805529-94e4e83f-a213-47cb-9431-5d8d3430058d.png">

1. จากหน้า dashboard คลิกเลือก Change it ในส่วน Master Password
2. กรอกรหัสผ่านเดิม และรหัสผ่านใหม่ 
3. กดยืนยัน change password

เราสามารถกลับมาที่ส่วนนี้ได้อีกครั้งจากเมนูด้านซ้ายมือ:
Security > Password > Active Master Password Provider > Change password


## เปลี่ยน Admin Password 

ส่วนที่จำเป็นต้องทำใน Production เราสามารถเปลี่ยน Admin Password ได้ทันทีหลังล๊อคอินเข้ามาแล้ว

1. จากหน้า dashboard คลิกเลือก Change it ในส่วน Admin password
2. กรอกรหัสผ่านในช่อง password และ confirm password 
3. กดยืนยัน Save

เราสามารถกลับมาที่ส่วนนี้ได้อีกครั้งจากเมนูด้านซ้ายมือ:
Security > Users, Groups, Roles > เลือก Users/Groups tab > เลือก Admin จากรายชื่อ User