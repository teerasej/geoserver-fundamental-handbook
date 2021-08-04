
# การ Export เป็น GeoJSON, CSV, Zipped Shapefile

## GeoJSON

```
http://localhost:8080/geoserver/Nextflow/ows?
service=WFS
&version=1.0.0
&request=GetFeature
&typeName=Nextflow%3Amain_road
&maxFeatures=50
&outputFormat=application%2Fjson
```

## KML 

```
http://localhost:8080/geoserver/Nextflow/ows?
service=WFS
&version=1.0.0
&request=GetFeature
&typeName=Nextflow%3Amain_road
&maxFeatures=50
&outputFormat=application/vnd.google-earth.kml+xml
```

## CSV

```
http://localhost:8080/geoserver/Nextflow/ows?
service=WFS
&version=1.0.0
&request=GetFeature
&typeName=Nextflow%3Amain_road
&maxFeatures=50
&outputFormat=csv
```

## Zipped Shapefile


```
http://localhost:8080/geoserver/Nextflow/ows?
service=WFS
&version=1.0.0
&request=GetFeature
&typeName=Nextflow%3Amain_road
&maxFeatures=50
&outputFormat=SHAPE-ZIP
```
