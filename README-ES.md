# Craftime para Android — proyecto inicial

Este proyecto envuelve el HTML que compartiste (`craft-time-58-survival-performance.html`)
en una aplicación Android usando WebView. El archivo se copia como `app/src/main/assets/index.html`.

## Qué incluye
- Nombre de aplicación: Craftime.
- Orientación horizontal.
- Pantalla completa inmersiva.
- JavaScript y DOM storage habilitados para el juego.
- El HTML se carga desde los recursos de la aplicación, por lo que el juego base puede abrir sin internet.
- Flujo de GitHub Actions para generar un APK de depuración en la nube.

## Cómo generar el APK usando solo el teléfono
1. Descarga y descomprime este ZIP en tu teléfono.
2. Crea un repositorio nuevo en GitHub desde el navegador.
3. Sube el contenido de esta carpeta al nivel raíz del repositorio, incluida la carpeta `.github`.
4. Abre la pestaña **Actions** y ejecuta **Build Craftime APK** (o espera a que termine tras subir a `main`).
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
