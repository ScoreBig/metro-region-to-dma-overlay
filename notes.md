ogr2ogr -f "GeoJSON" "MetroRegions.json" "MSSQL:server=servername;database=dbname;trusted_connection=yes" -sql "SELECT * FROM MetroRegion" -t_srs EPSG:4326
npm install -g topo-geo-json-converter geojson-merge
cat nielsentopo.json | topo-to-geo --pretty > nielsentopo.geojson
geojson-merge nielsentopo.geojson MetroRegions.json > combined.json