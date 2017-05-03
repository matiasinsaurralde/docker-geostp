<<<<<<< HEAD
docker-geostp
==============

Basado en el excelente trabajo realizado por Stefan Verhoeven <link>https://github.com/sverhoeven/docker-cartodb</link>

Este contenedor provee una version totalmente funcional en modo desarrollo del Portal de Información Georeferenciada
para Análisis de Políticas Públicas de la Secretaría Técnica de Planificación, dicho portal se basa en la herramienta
de software libre CARTO (anteriormente conocido como CartoDB) <link> https://github.com/CartoDB </link>.


Mediante este contenedor podes probar una versión totalmente funcional sin la necesidad de pasar por el doloroso proceso
de instalación.


Solo debes ejecutar los comandos y conectarte a http://geostp.localhost:3000 en tu navegador.

El login por defecto es desa/desa123.


Como construir el contenedor:
---------------------------

```
git clone https://github.com/raczajko/docker-geostp.git
docker build -t="raczajko/geostp" docker-geostp/
```

Como iniciar el contenedor:
-------------------------

```
docker run -d -p 3000:3000 -p 8080:8080 -p 8181:8181 raczajko/geostp
```

La instacia esta configurada con el hostname geostp.localhost, lo cual significa que el navegador debe poder resolver
 dicha dirección hacia el servidor donde corre la instancia.
 
Esto puede lograrse agregando el alias geostp.localhost a tu archivo de hosts.


Asumiendo que se levante localmente, para linux seria: 

```
sudo sh -c 'echo 127.0.1.1 geostp.localhost >> /etc/hosts'
```

O en windows en el archivo `C:\Windows\System32\drivers\etc\hosts`:

```
127.0.1.1 geostp.localhost
```
=======
# docker-geostp
Versión containerizada del Portal de Información Georeferenciada para Análisis de Políticas Públicas de la Secretaría Técnica de Planificación
>>>>>>> 4912ee79c1265e14646244f5602026193e9d3f50
