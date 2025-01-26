# QGIS Server

https://docs.qgis.org/3.34/en/docs/server_manual/containerized_deployment.html

docker network create qgis
docker run -d --rm --name qgis-server --net=qgis --hostname=qgis-server -v $(pwd)/data:/data:ro -p 5555:5555 -e "QGIS_PROJECT_FILE=/data/osm.qgs" qgis-server

from 
docker run -d --rm --name nginx --net=qgis --hostname=nginx -v $(pwd)/nginx.conf:/etc/nginx/conf.d/default.conf:ro -p 8080:80 nginx:1.13

# A scratch pad

This was a repo for a course lesson. It's repurposed as a scratchpad.

Filtering las files

## geemap
https://geemap.org/notebooks/101_lidar/

## laspy
https://laspy.readthedocs.io/en/latest/intro.html

## pdal
https://pdal.io/workshop/exercises/analysis/dtm/dtm.html?highlight=hillshade
