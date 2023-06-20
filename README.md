# tilemaker
Generate vector mbtiles use tilemaker.   1G pbf file spend about 110 minuis.
# Set settings
settings>-Actions->General->Workflow permissions->Read and Write permissions
# note:
   map sources:
   
     1  https://download.geofabrik.de/asia/china-latest.osm.pbf
     
     2  https://extract.bbbike.org/
     
    when from:
    
     http://download.openstreetmap.fr/extracts/
     
     Throw:
     
     "Can't read shapefiles unless a bounding box is provided.
     Error: Process completed with exit code 1.
     "
# use tiles-mbtiles
 tiles-mbtiles in ./data/tiles-mbtiles
 docker run --rm -it -v $(pwd)/data:/data -p 9090:8080 scanlidocker/tileserver-gl-light:v4.2.0 
 

# get tiles-mbtiles
cat tiles-mbtiles.tar.gz.aa >> tiles-mbtiles.tar.gz

gunzip tiles-mbtiles.tar.gz

tar xvf tiles-mbtiles.tar
