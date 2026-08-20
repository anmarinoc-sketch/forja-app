# Cómo obtener el .apk de FORJA (gratis, sin instalar nada en tu computador)

Esta carpeta ya tiene todo el código de la app nativa lista para compilarse. Vas a usar
**GitHub Actions**, un servicio gratuito que compila el APK por ti en la nube — tú no
instalas Android Studio ni nada pesado.

## Pasos

1. **Crea una cuenta gratis en [github.com](https://github.com)** si no tienes una (con tu correo).

2. **Crea un repositorio nuevo.** Botón verde "New" → ponle un nombre, por ejemplo
   `forja-app` → puede ser público o privado → clic en "Create repository".

3. **Sube todo el contenido de esta carpeta** al repositorio. La forma más simple:
   en la página del repositorio recién creado, busca el enlace
   "uploading an existing file", y arrastra ahí TODOS los archivos y carpetas que
   están junto a este documento (incluida la carpeta `.github`, que a veces no se ve
   porque empieza con un punto — asegúrate de incluirla, es la que dispara la compilación).

4. **Ve a la pestaña "Actions"** del repositorio (arriba). Si es la primera vez,
   te pedirá confirmar "I understand my workflows, go ahead and enable them" — acéptalo.

5. Debería aparecer un flujo llamado **"Build APK"** ejecutándose solo. Si no,
   entra a Actions → "Build APK" (a la izquierda) → botón "Run workflow".

6. **Espera unos 3–5 minutos.** Cuando el círculo se ponga verde ✓, haz clic
   en esa ejecución.

7. Baja hasta la sección **"Artifacts"** y descarga **forja-apk**. Va a bajar como
   un `.zip` — ábrelo, adentro está el archivo real: **`app-debug.apk`**.

Ese `app-debug.apk` es el archivo que le puedes compartir a cualquier persona por
WhatsApp, correo, USB, lo que sea. Ellos lo instalan directamente en su Android
(activando "permitir instalar de orígenes desconocidos" si el celular lo pide) y la
app funciona **completamente offline**, sin necesidad de que esté hospedada en
ningún lado — todo (incluidas las gráficas) viene empaquetado dentro del propio
archivo. Los datos que cada persona registre se guardan en su propio celular.

## Nota

Este es un APK de tipo "debug" — perfecto para instalar y compartir directamente
así. No es el mismo tipo de paquete que exige Google Play Store (eso requeriría
firmarlo con una clave de publicación y seguir el proceso de la tienda, que es
un tema aparte).
