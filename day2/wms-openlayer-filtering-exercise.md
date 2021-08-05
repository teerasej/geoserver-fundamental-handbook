
# Exercise: การ Filter ข้อมูล

## Layer 

1. [ลงชื่อเข้าใช้ GeoServer](../day1/login-admin-firsttime.md)
2. เข้าไปที่ **Data > Layer Preview**
3. ค้นหา Layer ชื่อ **topp:tasmania_water_bodies**
4. เลือก Common Formats เป็น **OpenLayers**

จากส่วนนี้กดปุ่ม **...** เพื่อเปิด Tool bar ขึ้นมา เครื่องมือที่เห็นคือ Parameter ที่สามารถส่งมาพร้อมกับ request ได้ 

5. เปิด Filter เลือก **CQL** และกำหนดค่า ที่ต้องการ เช่น 

- AREA<1066494066
- AREA>1066494066

และกด **apply**

## Layer Group

1. เข้าไปที่ **Data > Layer Preview**
2. ค้นหา Layer ชื่อ **topp:tasmania_water_bodies**
3. เลือก Common Formats เป็น **OpenLayers**
4. จากส่วนนี้กดปุ่ม **...** เพื่อเปิด Tool bar ขึ้นมา เครื่องมือที่เห็นคือ Parameter ที่สามารถส่งมาพร้อมกับ request ได้ 

5. เปิด Filter เลือก **Feature ID** และกำหนดชื่อ Feature Id ที่ต้องการ เช่น 

```
tasmania_state_boundaries.1,tasmania_water_bodies.5
```

และกด **apply**

> เราไม่สามารถใช้ CQL กับ Layer Group ได้ วิธีคือให้ใช้ CQL กับ Layer ย่อยๆ แทน