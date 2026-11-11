# Visor de la Sagrada Biblia

Visor web local de la Sagrada Biblia (Cantera–Iglesias): navegación por libro y capítulo, búsqueda por referencia (`Is 7,14`), por palabra o por frase, y notas junto a cada versículo. Se instala como app en el celular y funciona sin conexión.

**Este repositorio no contiene el texto de la Biblia.** Cada persona carga su propio archivo `biblia.json` la primera vez; se guarda solo en el navegador de su dispositivo (IndexedDB) y no se envía a ningún servidor. El `.gitignore` excluye `biblia*.json` para evitar subirlo por accidente.

## Qué incluye
- **Lectura completa:** introducción general, introducción y secciones de cada libro, títulos de perícopa, pasajes paralelos, cursivas, inscripciones de los salmos y versos partidos (`4b`), como en la edición impresa.
- **Notas:** al tocar el número de una nota se abre bajo el versículo; en *Ajustes* se pueden mostrar todas (en pantalla ancha van al margen); el botón *Notas del capítulo* las lista juntas. Las referencias dentro de las notas (por ejemplo «Is. 65. 17») son enlaces.
- **Búsqueda:** referencias (`Gn 1,26`, `1 Re 3:4-6`, `sal 23`), palabras sin importar acentos o mayúsculas (todas deben aparecer) y frases entre comillas. Los botones *Texto* y *Notas* limitan dónde se busca.
- **Comodidades:** tema claro/oscuro, tamaño de letra, copiar un versículo (tocar su número), impresión, retomar la lectura donde se dejó.

## Publicar con GitHub Pages
1. Crea un repositorio en GitHub y sube estos archivos (`index.html`, `sw.js`, `manifest.webmanifest`, los tres `.png`, `.gitignore` y este README). **No subas `biblia.json`.**
2. En el repositorio: *Settings → Pages → Build and deployment → Deploy from a branch → `main` / `(root)`*.
3. En un minuto, la app queda en `https://TU-USUARIO.github.io/NOMBRE-DEL-REPO/`.

## Usarla en el celular
1. Abre el enlace en el celular (Safari en iPhone, Chrome en Android).
2. Instálala: Safari → Compartir → *Añadir a pantalla de inicio*; Chrome → menú ⋮ → *Instalar aplicación*.
3. Abre la app, toca *Elegir el archivo biblia.json* y selecciónalo (cópialo antes al celular por AirDrop, correo, Drive, etc.).
4. Listo: desde ahí funciona sin conexión. En iPhone conviene instalarla en la pantalla de inicio, porque Safari puede borrar los datos de sitios que no se usan en una semana.

## Notas técnicas
- El archivo de datos es JSON de «formato 2». La app rechaza archivos de versiones anteriores y avisa.
- Al publicar una versión nueva, el navegador actualiza la interfaz solo; el texto guardado en el dispositivo no se pierde.
