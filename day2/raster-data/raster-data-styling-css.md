
# การทำ Styling Raster Data ด้วย CSS


## เตรียมข้อมูล 

1. ให้ทำการสร้าง Store แบบ **GeoTIFF**
2. เลือกไฟล์ชื่อ **srtm_boulder.tiff** จาก directory ชื่อ **mosaic_single_tiff**
3. กำหนดสร้าง layer ให้เรียบร้อย


## Styling ด้วย CSS 

workshop นี้ต้อง[ผ่านการติดตั้ง CSS Extension ในขั้นตอนนี้แล้ว](../../day1/add-extension.md)

1. จากหน้าเว็บ **GeoServer > Data > Styles** และคลิก **Add New Style**
2. ตั้งชื่อ Style ว่า **srtm css**
3. กำหนด format เป็น **CSS** 
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
