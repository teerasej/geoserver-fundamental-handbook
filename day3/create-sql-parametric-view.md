
# การสร้าง SQL Parametric View based Layer

- ต้องทำการสร้าง Store จาก PostGIS Database [ใน workshop นี้แล้ว](create-layer-from-postgis.md)

1. [login เข้าใช้งาน GeoServer](../day1/login-admin-firsttime.md)
2. จากเมนูด้านซ้าย เลือก **Data > Layers**
3. กด **Add a new layer**
4. เลือก Store เป็น **Nextflow:nyc_buildings**
5. ในส่วนนี้ แทนที่จะ publish ตาม layer ที่ให้มาโดยตรง ให้เลือก **Configure new SQL view...**