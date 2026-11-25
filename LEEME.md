# Fotos a PDF: proyecto para compilar el APK

Contiene la app (carpeta `www`) y el proyecto Android ya armado (carpeta `android`).
No necesitas hosting ni instalar nada en tu computadora.

## Opción A: GitHub compila el APK por ti (gratis, unos 5 a 10 minutos)

1. Crea una cuenta en github.com (si no tienes) y un repositorio nuevo, por ejemplo `fotos-pdf`.
   Puede ser privado.
2. En el repositorio: **Add file > Upload files** y arrastra TODO el contenido de esta carpeta
   (que incluye `www`, `android`, `package.json`, `capacitor.config.json` y la carpeta oculta `.github`).
   Si `.github` no se sube (algunos navegadores ignoran las carpetas ocultas):
   **Add file > Create new file**, escribe el nombre `.github/workflows/build-apk.yml`
   y pega el contenido del archivo `build-apk.yml` de esta carpeta.
3. Haz clic en **Commit changes**.
4. Abre la pestaña **Actions**. Verás "Compilar APK" ejecutándose. Si no arranca,
   entra a "Compilar APK" y pulsa **Run workflow**.
5. Cuando salga el check verde, entra a esa ejecución y abajo, en **Artifacts**, descarga `FotosPDF-apk`.
   Es un ZIP: descomprímelo y dentro está `app-debug.apk`.
6. Pásalo al celular e instálalo. Android te pedirá permitir "instalar apps de origen desconocido".

## Opción B: con Android Studio en tu computadora

Abre la carpeta `android` con Android Studio y usa **Build > Build APK(s)**.

## Cómo se usa la app

- Al abrirla pide permiso de cámara: acepta.
- Elige el intervalo y toca Empezar. Toma las fotos solas.
- "Página completada" cierra la hoja. "Generar PDF" termina.
- "Guardar o enviar PDF" abre el menú de Android: guárdalo en Archivos o Drive, o envíalo por WhatsApp, correo, etc.

## Notas

- Es un APK de prueba (debug): sirve perfecto para instalar en tu celular, pero no se puede subir a Play Store.
- Si el APK no compila, copia el mensaje de error de la pestaña Actions y lo corrijo.
