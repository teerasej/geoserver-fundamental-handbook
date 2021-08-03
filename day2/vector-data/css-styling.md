
# การทำ Styling map

## ด้วย QGIS 

การทำงานตรงส่วนนี้ต้องทำ [Exercise shapefile](../../day1/exercise-publish-shapfile.md) เสร็จก่อน

### โหลด Layer

1. เปิด QGIS
2. สร้างการเชื่อมต่อแบบ WFS ไปที่ **http://localhost:8080/geoserver/nextflow/wfs**
3. ทำการเพิ่ม **MainRoad** layer เข้ามาในโปรเจค 

### ปรับแต่ง style

4. คลิกขวาที่ **Main Road** Layer และเลือก **Show Attribute Layer**
5. ให้สังเกตว่า Layer นี้มี attribute ชื่อ **LABEL_NAME** ติดมาด้วย

<img width="414" alt="2021-08-03_20-51-57" src="https://user-images.githubusercontent.com/85179/128027356-a66c4501-2dbc-4251-91e0-3052c284c48e.png">


7. คลิกขวาที่ **Main Road** Layer และเลือก **Properties**

<img width="428" alt="2021-08-03_20-52-34" src="https://user-images.githubusercontent.com/85179/128027424-df42691e-cb59-4761-a89a-85325d1add36.png">


9. ในส่วน **Symbology** ทดลองปรับแต่ง line และกด **apply**

<img width="822" alt="2021-08-03_20-50-18" src="https://user-images.githubusercontent.com/85179/128027643-8255004b-58c8-4198-a23e-98fa45136a60.png">


10. ในส่วน **Labels** เลือก **single labels**

<img width="824" alt="2021-08-03_20-50-30" src="https://user-images.githubusercontent.com/85179/128027812-1d9d8f72-9c39-461b-8396-612baeb1638c.png">


11. ทดลองกำหนด style ให้ **LABEL_NAME** และกด **apply**

<img width="824" alt="2021-08-03_20-51-22" src="https://user-images.githubusercontent.com/85179/128027871-99fbc162-c8ef-448c-8e9f-6065ecfbb73c.png">


### บันทึกและเอาไปใช้ใน GeoServer

9.  ด้านล่างกดปุ่ม **Style** และเลือก **Save Style...**

<img width="188" alt="2021-08-03_20-48-43" src="https://user-images.githubusercontent.com/85179/128027937-0982fe47-02a6-4497-8736-df2b1024330c.png">


11. เลือก **Save style as SLD file** และกำหนดที่อยู่ของไฟล์

<img width="631" alt="2021-08-03_20-49-16" src="https://user-images.githubusercontent.com/85179/128028072-5a5f42cb-4dfc-48bd-8027-3d6cb40c788c.png">


12. กลับมาที่หน้าเว็บ GeoServer 
13. เลือก **Data > Styles > Add New Styles**
14. ตั้งชื่อ Style และเลือก format เป็น **SLD**
15. ในส่วน **Upload a style file** ให้เลือกไฟล์ SLD ที่ได้จาก QGIS และกด **upload** จะเห็นว่าโค้ด SLD แสดงขึ้นมาในส่วนด้านล่าง

<img width="749" alt="2021-08-03_20-57-40" src="https://user-images.githubusercontent.com/85179/128028390-fe6314eb-0f5b-4a85-af8a-9512e61d2578.png">


16. กด **Layer Preview** tab และเลือก **Main Road** Layer 

## ด้วย CSS

workshop นี้ต้อง[ผ่านการติดตั้ง CSS Extension ในขั้นตอนนี้แล้ว](../../day1/add-extension.md)

1. [login เข้าใช้งาน GeoServer](../../day1/login-admin-firsttime.md)
2. จากเมนูด้านซ้าย เลือก **Data > Styles**
3. กด **Add new style**
4. กำหนดค่าตามนี้ 

- **Name**: css_main_road
- **Format**: CSS

5. ใน Style Editor เขียน CSS ตามนี้ 

```css
* {
  stroke: orange;
  stroke-width: 6;
  stroke-linecap: round;
}
```

6. กด **apply** 
7. เลือก **Layer Preview** tab และเลือก **MainRoad** layer 

## Exercise 

ทดสอบปรับ CSS Rule เป็นแบบด้านล่าง และพรีวิว

```css
* {
  stroke: orange, yellow;
  stroke-width: 6, 2;
  stroke-linecap: round;
  z-index: 1, 2;
}
```

```css
* {
  stroke: orange, yellow;
  stroke-width: 6, 2;
  stroke-linecap: round;
  z-index: 1, 2;
  label: [LABEL_NAME];
  font-fill: black;
  font-family: Arial;
  font-size: 12;
  font-weight: bold;
  halo-color: white;
  halo-radius: 2;
  -gt-label-follow-line: true;
  -gt-label-group: true;
  -gt-label-repeat: 400;
  -gt-label-max-displacement: 50;
}
```
