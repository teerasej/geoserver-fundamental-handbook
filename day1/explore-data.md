
# สำรวจแหล่งข้อมูล Workspace, Store, และ Layer

การเข้าใช้งานส่วนนี้ได้ [จะต้อง Login เข้าใช้งานก่อน](login-admin-firsttime.md)

## Workspace

1. จากเมนูด้านซ้าย เลือก Data > Workspaces
2. เลือก tiger
3. สำรวจรายละเอียดสำคัญ

    - **Namespace URI** กำหนด URI จำเพาะให้กับ workspace, ไม่จำเป็นต้องเป็น URL ที่มีอยู่จริงๆ
    - **Setting & Services** โดยปกติจะใช้ global configuration ถ้าเลือกตรงนี้จะเป็นการสร้าง local configuration

## Store 

1. จากเมนูด้านซ้าย เลือก Data > Stores
2. สังเกตว่า Store จะผูกอยู่กับ Workspace
3. คลิกเลือก Store ชื่อ **sf**

    - สังเกตว่าเป็น Vector Data Source แบบ Shapefile
    - ส่วน Connection Parameter จะมีการตั้งค่าชี้ไปที่ไฟล์ (ในที่นี้สามารถเป็น URL ได้)


3. กลับออกมาที่หน้า Store คลิกเลือก Store ชื่อ **sfdem**

    - สังเกตว่าเป็น Raster Data Source
    - ส่วน Connection Parameter จะมีการตั้งค่าชี้ไปที่ไฟล์ (ในที่นี้สามารถเป็น URL ได้)

4. สังเกตว่าในที่นี้ ไม่มี Store ที่เป็นแบบ PostGIS เพราะไม่มีการทำงานร่วมกับฐานข้อมูล

## การพรีวิวดูข้อมูล Layer และ Layer group

### Layer

1. จากเมนูด้านซ้าย เลือก Data > Layers
2. สังเกตว่า Layer จะผูกอยู่กับ Store
3. สังเกตว่า name และ title ของ Layer จะต่างกัน โดย name จะเป็นชื่อที่ใช้ในระบบจริงๆ ส่วน title เป็นชื่อที่อ่านง่ายกว่าสำหรับมนุษย์
4. ด้านหน้าของ Layer จะมีไอคอนบอก[ประเภทของ Layer](https://docs.geoserver.org/latest/en/user/data/webadmin/layers.html#layer-types) ไว้ 

<img width="250" alt="2021-08-02_13-40-13" src="https://user-images.githubusercontent.com/85179/127815360-1e242408-b10c-494b-b9b7-ec42c609be64.png">



### Layer Group

1. จากเมนูด้านซ้าย เลือก Data > Layer Groups
2. สังเกตว่า Layer groups จะไม่ผูกกับอะไรเลย
3. เลือกเปิดดู spearfish
4. สังเกตรายละเอียดในส่วน Layer ที่มีการเลือก Layer ทั่วไปมาซ้อนกัน และสามารถจัดลำดับได้