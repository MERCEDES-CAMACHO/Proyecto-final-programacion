# Proyecto-final-programacion
En este trabajo nos centraremos en la comparación de datos de Senamhi  de  algunas provincias del departamento de Cusco con data Pisco. Nos centraremos en data de precipitación y temperatura.
Este trabajo fue realizado por los siguientes estudiantes:
Camacho Vega  Mercedes Emerita
Huayllani  Panuera Dialdina
León Chaiña  Lisbeth Karola
Ramos Cerna Alejandra Gianella

    install.packages(c("raster", "ncdf4"))
    long_lat <- read.csv("estaciones_c.csv", header = T)
    View(long_lat)
    raster_pp   <- raster::brick("FINAL/DATA GRILLADA/Precipitacion/Mensual/Prec.nc")
    raster_tmax <- raster::brick("FINAL/DATA GRILLADA/Temperatura/Mensual/Tmax.nc")
    raster_tmin <- raster::brick("FINAL/DATA GRILLADA/Temperatura/Mensual/Tmin.nc")
    sp::coordinates(long_lat) <- ~XX+YY
    raster::projection(long_lat) <- raster::projection(raster_pp)
    raster::projection(long_lat) <- raster::projection(raster_tmax)
    raster::projection(long_lat) <- raster::projection(raster_tmin)
    raster::projection(long_lat) <- raster::projection(raster_pp)
    raster::projection(long_lat) <- raster::projection(raster_tmax)
    raster::projection(long_lat) <- raster::projection(raster_tmin)

![Rplot](https://user-images.githubusercontent.com/78572913/107041783-e7fbfc00-678e-11eb-8c91-02ac8af39e89.png)
