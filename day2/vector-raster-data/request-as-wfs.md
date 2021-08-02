
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



2. คลิกขวา และเลือก **Properties** สังเกตว่าสามารถปรับแต่งข้อมูลของแผนที่ได้ 



3. สังเกตเทียบกับ Layer จาก WMS