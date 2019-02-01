# Reprojections with GDAL

Shapefiles show geometries according to Spatial Reference Systems (SRS)
To compare shapefiles one would need to be using the same SRS

System Requires:
+ python3
+ gdal


Python Requires:
+ gdal
+ shapely
+ jupyter


## Installing GDAL
```bash
sudo dnf install -y gdal-devel.x86_64 gcc-c++
cd /tmp
pip download  GDAL==$(gdal-config --version | awk -F'[.]' '{print $1"."$2}')
tar -xvzf GDAL-<version>.tar.gz
cd GDAL-<version>
python setup.py build_ext --include-dirs=/usr/include/gdal/
python setup.py install
```
