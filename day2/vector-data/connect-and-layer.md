
# การเชื่อมต่อ และโหลด Layer

ในที่นี้เราสามารถใช้ QGIS ซึ่งเป็น Open Source และฟรีในการทดสอบเชื่อมต่อกับ Protocol ต่างๆ ได้

1. เปิด QGIS
2. ไปที่เมนู **Layer > Add Layers > Add WMS/WMTS Layer**
3. ในส่วน **Server Connection** เลือก **New**
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

7. ถ้ากดบริเวณพื้นที่ water bodies จะเป็นการขอ Attribute เพิ่มเติมจาก GeoServer
8. สามารถ double click ที่ layer เพื่อปรับเปลี่ยน Style ได้
