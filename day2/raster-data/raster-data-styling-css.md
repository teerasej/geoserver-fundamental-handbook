
# การทำ Styling Raster Data 


## เตรียมข้อมูล 

1. ให้ทำการสร้าง Store แบบ GeoTIFF
2. เลือกไฟล์ชื่อ **srtm_boulder.tiff** จาก directory ชื่อ **mosaic_single_tiff**
3. กำหนดสร้าง layer ให้เรียบร้อย


## ด้วย CSS 

workshop นี้ต้อง[ผ่านการติดตั้ง CSS Extension ในขั้นตอนนี้แล้ว](../../day1/add-extension.md)

1. จากหน้าเว็บ GeoServer > Data > Styles และสร้าง Style ใหม่
2. ตั้งชื่อ Style ว่า **srtm css**
3. กำหนด format เป็น CSS 
4. เขียน CSS Rule ตามด้านล่าง 

```css
* {
   raster-channels: auto;
   raster-color-map:
     color-map-entry(black, 0, 0)
     color-map-entry(green, 1500)

     color-map-entry(yellow, 2000)
     color-map-entry(maroon, 3000)
     color-map-entry(white, 4000);
}
```

5. กด apply
6. เปิด Layer Preview tab และเลือก **strm_boulder** layer

## ด้วย QGIS

1. เปิด QGIS
2. ใช้การเชื่อมต่อ WCS ไปที่ **http://localhost:8080/geoserver/nextflow/wcs**
3. เลือกเพิ่ม strm_boulder layer ลงโปรเจค
4. คลิกขวาที่ layer > properties...

### กำหนดค่าสี

5. เลือก Symbology
6. กำหนดค่าตามด้านล่าง

- Render type: Singleband pseudocolor
- Interpolation: Linear
- Color Ramp: เลือกตามต้องการ (หรือจะเลือกกดเพิ่มจากส่วนปุ่ม + ด้านล่าง หรือ Classify เพื่อให้คำนวนค่าก็ได้)
- กด Apply 

### บันทึกและเอาไปใช้ใน GeoServer

7.  ด้านล่างกดปุ่ม **Style** และเลือก **Save Style...**

<img width="188" alt="2021-08-03_20-48-43" src="https://user-images.githubusercontent.com/85179/128027937-0982fe47-02a6-4497-8736-df2b1024330c.png">


8. เลือก **Save style as SLD file** และกำหนดที่อยู่ของไฟล์

<img width="631" alt="2021-08-03_20-49-16" src="https://user-images.githubusercontent.com/85179/128028072-5a5f42cb-4dfc-48bd-8027-3d6cb40c788c.png">


9. กลับมาที่หน้าเว็บ GeoServer 
10. เลือก **Data > Styles > Add New Styles**
11. ตั้งชื่อ Style และเลือก format เป็น **SLD**
12. ในส่วน **Upload a style file** ให้เลือกไฟล์ SLD ที่ได้จาก QGIS และกด **upload** จะเห็นว่าโค้ด SLD แสดงขึ้นมาในส่วนด้านล่าง

<img width="749" alt="2021-08-03_20-57-40" src="https://user-images.githubusercontent.com/85179/128028390-fe6314eb-0f5b-4a85-af8a-9512e61d2578.png">

13. กด **Layer Preview** tab และเลือก **strm_boulder** layer