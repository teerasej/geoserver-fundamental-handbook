
# การเชื่อมต่อแบบ WFS

การเชื่อมต่อแบบนี้จะไม่ได้ Layer มาเป็นรูปภาพอย่างเดียว แต่จะมีข้อมูลของ layer นั้นๆ เช่น attribute และ feature ติดมาด้วย 

1. เชื่อมต่อไปที่ GeoServer แต่คราวนี้ให้เชื่อมต่อแบบ WFS
2. ใช้ข้อมูลตามด้านล่าง 

- **Name**: Tasmania WFS
- **URL**: http://localhost:8080/geoserver/topp/wfs
- **Authentication** > **Basic**
  - **Username**: admin
  - **Password**: รหัสผ่านที่ตั้งไว้

5. กดปุ่ม **Connect**
6. เลือก Layer มาใส่ในโปรเจค

- Tasmania water bodies จาก Tasmania WFS
- Tasmania water bodies จาก Tasmania
- Tasmania state boundaries

## การใช้งาน Layer จาก WPS

1. คลิกขวา และเลือก **Show Attribute Table**

<img width="490" alt="2021-08-02_22-41-27" src="https://user-images.githubusercontent.com/85179/127888575-a778d576-7901-424e-b791-0d881a1ee9b1.png">


2. คลิกขวา และเลือก **Properties** สังเกตว่าสามารถปรับแต่งข้อมูลของแผนที่ได้ 

<img width="504" alt="2021-08-02_22-43-41" src="https://user-images.githubusercontent.com/85179/127888600-bbcd823e-33d5-4236-bdd2-502c875ddda0.png">


4. เปิดเมนู Vector > Geoprocessing > Buffer 

<img width="438" alt="2021-08-02_22-49-01" src="https://user-images.githubusercontent.com/85179/127889384-9655650f-81cc-470a-a667-68702f5da794.png">


5. เลือก input layer สังเกตว่าจะเลือกได้แค่ layer ที่มาจาก WFS และกรอกค่า distance เป็น 0.01 จากนั้นกดปุ่ม Run 
<img width="687" alt="2021-08-02_22-49-24" src="https://user-images.githubusercontent.com/85179/127889320-0c42c280-59f9-40c2-9d82-9ac70fd58596.png">


6. จะได้ layer buffer มาใช้งาน

<img width="301" alt="2021-08-02_22-53-24" src="https://user-images.githubusercontent.com/85179/127889495-e65d2412-b909-422d-9a54-8ee522f35a29.png">


7. สังเกตเทียบกับ Layer จาก WMS
