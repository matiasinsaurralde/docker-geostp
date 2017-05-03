docker-geostp
==============

Basado en el excelente trabajo realizado por Stefan Verhoeven: [docker-cartodb](https://github.com/sverhoeven/docker-cartodb).

Este contenedor provee una versión totalmente funcional en modo desarrollo del Portal de Información Georeferenciada
para Análisis de Políticas Públicas de la Secretaría Técnica de Planificación, dicho portal se basa en la herramienta
de software libre CARTO (anteriormente conocida como [CartoDB](https://github.com/CartoDB)).

Mediante este contenedor podes probar una versión totalmente funcional sin la necesidad de pasar por el doloroso proceso
de instalación.


Sólo debes ejecutar los comandos y conectarte a http://geostp.localhost:3000 en tu navegador.

El login por defecto es:

**Usuario:** desa

**Contraseña:** desa123

Cómo construir el contenedor:
---------------------------

```
$ git clone https://github.com/raczajko/docker-geostp.git
$ docker build -t="raczajko/geostp" docker-geostp/
```

Cómo iniciar el contenedor:
-------------------------

```
$ docker run -d -p 3000:3000 -p 8080:8080 -p 8181:8181 raczajko/geostp
```

La instancia está configurada con el hostname `geostp.localhost`, lo cual significa que el navegador debe poder resolver
 dicha dirección hacia el servidor donde corre la instancia.
 
Esto puede lograrse agregando el alias `geostp.localhost` a tu archivo de hosts.

Asumiendo que se levante localmente, para Linux sería:

```sh
$ sudo sh -c 'echo 127.0.1.1 geostp.localhost >> /etc/hosts'
```

O para Windows, `C:\Windows\System32\drivers\etc\hosts`:

```
127.0.1.1 geostp.localhost
```
