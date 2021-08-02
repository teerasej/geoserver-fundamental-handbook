
# การเชื่อมต่อ และโหลด Layer

ในที่นี้เราสามารถใช้ QGIS ซึ่งเป็น Open Source และฟรีในการทดสอบเชื่อมต่อกับ Protocol ต่างๆ ได้

1. เปิด QGIS
2. ไปที่เมนู **Layer > Add Layers > Add WPS Layer**

<img width="595" alt="2021-08-02_17-32-37" src="https://user-images.githubusercontent.com/85179/127880010-167fef6c-74e3-4553-a451-68e14fdf1f6a.png">


3. ในส่วน **Server Connection** เลือก **New**

<img width="498" alt="2021-08-02_17-32-59" src="https://user-images.githubusercontent.com/85179/127880036-5f37cac8-28fd-403b-b91e-c962c503dff4.png">


4. กรอกข้อมูล และกด OK

- **Name**: Tasmania
- **URL**: http://localhost:8080/geoserver/topp/wms
- **Authentication** > **Basic**
  - **Username**: admin
  - **Password**: รหัสผ่านที่ตั้งไว้

5. กดปุ่ม **Connect**
6. เลือก **Add Layer** ทีละอันตามลำดับมาใส่ในโปรเจค

- Tasmania state boundaries
- Tasmania water bodies
- Tasmania cities

<img width="644" alt="2021-08-02_17-35-34" src="https://user-images.githubusercontent.com/85179/127880067-3ea87c1e-a2d3-4671-a853-f1d0cdb4386a.png">


7. ถ้ากดบริเวณพื้นที่ water bodies จะเป็นการขอ Attribute เพิ่มเติมจาก GeoServer
8. สามารถ double click ที่ layer เพื่อปรับเปลี่ยน Style ได้
