## Autor King Pitiki OFC | Hack Purgatory
## Licencia y Aviso Legal
Este proyecto se publica únicamente con fines de investigación, aprendizaje e ingeniería inversa. Su contenido está destinado al estudio del funcionamiento interno de aplicaciones Android, la seguridad informática y el análisis de software.

No se promueve ni se autoriza el uso de este proyecto para infringir derechos de autor, eludir mecanismos de protección, distribuir software modificado sin autorización o realizar actividades que vulneren la legislación vigente o los términos de servicio de terceros.

Cada usuario es el único responsable del uso que haga de la información y herramientas aquí presentadas.

© 2026 King Pitiki OFC | Hack Purgatory. Todos los derechos reservados.

## Tutorial

-> extraer en formato .apk la aplicación de XRecorder en su última versión actual 2.5.3.2

-> matar verification de firma con la herramienta MT Manager.

clave de firma: predeterminado
esquema: V1+V2+V3
usar versión mejorada [activa]

-> Dentro de los archivos internos que componen la aplicación de XRecorder.apk eliminar los archivos:

```DebugProbesKt.bin
androidsupportmultidexversion.txt
billing.properties
core-common.properties
feature-delivery.properties
firebase-abt.properties
firebase-analytics.properties
firebase-annotations.properties
firebase-appcheck-interop.properties
firebase-auth-interop.properties
firebase-common.properties
firebase-components.properties
firebase-config.properties
firebase-crashlytics.properties
firebase-encoders-json.properties
firebase-encoders-proto.properties
firebase-encoders.properties
firebase-installations-interop.properties
firebase-installations.properties
firebase-measurement-connector.properties
firebase-storage.properties
kotlin-tooling-metadata.json
play-services-ads-api.properties
play-services-ads-identifier.properties
play-services-ads.properties
play-services-appset.properties
play-services-auth-api-phone.properties
play-services-auth-base.properties
play-services-auth.properties
play-services-base.properties
play-services-basement.properties
play-services-fido.properties
play-services-location.properties
play-services-measurement-api.properties
play-services-measurement-base.properties
play-services-measurement-impl.properties
play-services-measurement-sdk-api.properties
play-services-stats.properties
play-services-measurement-sdk.properties
play-services-measurement.properties
play-services-places-placereport.properties
play-services-tasks.properties
stamp-cert-sha256
transport-api.properties
transport-backend-cct.properties
transport-runtime.properties
user-messaging-platform.properties
```


-> y eliminar las carpetas:

```
com
Javax
okhttp3
org
```

-> importar patch1 a classes.dex
com/inshot/screenrecorder/iab/c$e

-> importar patch2 a classes.dex
QC0

-> guardar y firmar la ampliación

clave de firma: predeterminado 
esquema: V3 (Android 9.0+)

-> Finalmente se desinstala la aplicación original de XRecorder (si ya está instalado) y se instala el XRecorder modificado (aceptar los permisos de instalar de todas formas)


