# QGIS Server

https://docs.qgis.org/3.34/en/docs/server_manual/containerized_deployment.html

from  ~/qgis-server/

docker network create qgis
docker run -d --rm --name qgis-server --net=qgis --hostname=qgis-server -v $(pwd)/data:/data:ro -p 5555:5555 -e "QGIS_PROJECT_FILE=/data/osm.qgs" qgis-server
 
docker run -d --rm --name nginx --net=qgis --hostname=nginx -v $(pwd)/nginx.conf:/etc/nginx/conf.d/default.conf:ro -p 8080:80 nginx:1.13


![image](https://github.com/user-attachments/assets/d9ccbc59-0eaf-4bd2-bf9b-02b6cff98962)

# A scratch pad

This was a repo for a course lesson. It's repurposed as a scratchpad.

Filtering las files

## geemap
https://geemap.org/notebooks/101_lidar/

## laspy
https://laspy.readthedocs.io/en/latest/intro.html

## pdal
https://pdal.io/workshop/exercises/analysis/dtm/dtm.html?highlight=hillshade
