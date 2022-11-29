# tilemaker
make vector mbtiles with tilemaker
note:
   map src:
     1  https://download.geofabrik.de/asia/china-latest.osm.pbf
     2  https://extract.bbbike.org/
    no in
     http://download.openstreetmap.fr/extracts/
     "Can't read shapefiles unless a bounding box is provided.
     Error: Process completed with exit code 1.
     "

root@node-1:/home/tileserver-gl# docker run --rm -it -v $(pwd):/data -p 9090:8080 scanlidocker/tileserver-gl-light:v4.2.0 --mbtiles ./data/tiles.mbtiles

cat tiles-mbtiles.tar.gz.aa >> tiles-mbtiles.tar.gz

gunzip tiles-mbtiles.tar.gz

tar xvf tiles-mbtiles.tar
