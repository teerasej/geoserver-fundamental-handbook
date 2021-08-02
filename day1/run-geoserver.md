
# การเปิดปิด GeoServer (MacOS)

1. เปิดโปรแกรม Terminal มาที่โฟลเดอร์ของ Geoserver
2. รันคำสั่งด้านล่าง 

```bash
cd bin
sh startup.sh
```

3. จะมี Log แสดงการทำงานของ Geoserver 
4. ถ้าการทำงานไม่มีปัญหา จะมีการแสดงข้อความประมาณด้านล่างในบรรทัดสุดท้าย 

```bash
INFO:oejs.Server:main: Started @19203ms
```

5. ทดสอบเปิดเว็บเบราเซอร์มาที่ URL [http://localhost:8080/geoserver](http://localhost:8080/geoserver)