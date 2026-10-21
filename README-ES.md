# Craftime para Android — proyecto inicial

Este proyecto envuelve el HTML que compartiste (`craft-time-58-survival-performance.html`)
en una aplicación Android usando WebView. El archivo se copia como `app/src/main/assets/index.html`.

## Qué incluye
- Nombre de aplicación: Craftime.
- Orientación horizontal.
- Pantalla completa inmersiva.
- JavaScript y DOM storage habilitados para el juego.
- El HTML se carga desde los recursos de la aplicación, por lo que el juego base puede abrir sin internet.
- Menús con desplazamiento y tamaños compactos en horizontal para evitar que queden cortados.
- Ajustes conservadores de WebView para usar aceleración por hardware y reducir la presión del renderizador.
- Flujo de GitHub Actions para generar un APK de depuración en la nube.

## Cómo generar el APK usando solo el teléfono
1. Descarga y descomprime este ZIP en tu teléfono.
2. Crea un repositorio nuevo en GitHub desde el navegador.
3. Sube el contenido de esta carpeta al nivel raíz del repositorio, incluida la carpeta `.github`.
4. Abre la pestaña **Actions** y ejecuta **Build Craftime APK** (o espera a que termine tras subir a `master`).
5. Cuando termine correctamente, abre la ejecución y descarga el artefacto `Craftime-debug-apk`.
6. Dentro del ZIP descargado estará `app-debug.apk`. Instálalo en Android permitiendo instalaciones desde esa fuente si el sistema lo solicita.

## Importante
- Este es un proyecto fuente preparado para compilar, no un APK ya compilado.
- No se ha compilado ni probado en un dispositivo en esta sesión.
- El juego HTML original se conserva; todavía no se ha rediseñado su menú interno.
- Las funciones que dependan de servidores externos pueden requerir internet.
- La aplicación está configurada en horizontal para coincidir con el juego; cambia `screenOrientation` si prefieres otra orientación.
- Para una publicación de producción conviene generar una firma propia y revisar los permisos y políticas de privacidad.

## Si la compilación falla
Abre los logs de GitHub Actions y comparte aquí el primer error rojo completo. Podemos corregir la configuración o el código.


## Actualizar Craftime sin repetir todo el proceso
1. Reemplaza `app/src/main/assets/index.html` por la nueva versión del HTML.
2. Guarda y sube los cambios al repositorio en la rama `master`.
3. Abre **Actions** y descarga el artefacto `Craftime-debug-apk` cuando termine.
4. Instala el APK actualizado. Para que Android permita actualizar encima de la versión anterior, los APK deben conservar la misma firma de depuración; si cambia la firma, Android puede pedir desinstalar la anterior.

La mejora visual se ha añadido mediante CSS adaptable sin reescribir las mecánicas del juego. El rendimiento puede variar según el dispositivo y debe comprobarse en el teléfono.
