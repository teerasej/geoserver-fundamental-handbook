
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
6. คลิกขวาที่ **Main Road** Layer และเลือก **Properties**
7. ในส่วน **Symbology** ทดลองปรับแต่ง line และกด **apply**
8. ในส่วน **Labels** ทดลองกำหนด style ให้ **LABEL_NAME** และกด **apply**

### บันทึกและเอาไปใช้ใน GeoServer

9.  ด้านล่างกดปุ่ม **Style** และเลือก **Save Style...**
10. เลือก **Save style as SLD file** และกำหนดที่อยู่ของไฟล์
11. กลับมาที่หน้าเว็บ GeoServer 
12. เลือก Data > Styles > Add New Styles
13. ตั้งชื่อ Style และเลือก format เป็น SLD
14. ในส่วน Upload a style file ให้เลือกไฟล์ SLD ที่ได้จาก QGIS และกด upload จะเห็นว่าโค้ด SLD แสดงขึ้นมาในส่วนด้านล่าง
15. กด Layer Preview tab และเลือก Main Road Layer 

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