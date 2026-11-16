# Mi Autocaravana · Kentucky Corral 8

Web sin login para registrar mantenimiento, averías, gastos, viajes y referencias de documentos, con diseño adaptable a móviles y soporte PWA.

## Probar

Abre `index.html` en tu navegador. Para probar la instalación PWA, usa un servidor local (`python -m http.server 8000`) o publícala en GitHub Pages.

## Publicar en GitHub Pages (igual que la aplicación de Lucía)

1. Crea un repositorio nuevo en GitHub, por ejemplo `mi-autocaravana`.
2. Sube **los cuatro archivos** de este directorio a la raíz del repositorio (`index.html`, `manifest.webmanifest`, `sw.js`, `icon.svg`).
3. En **Settings → Pages**, selecciona **Deploy from a branch**, rama `main`, carpeta `/(root)` y guarda.
4. GitHub te mostrará la URL `https://TU_USUARIO.github.io/mi-autocaravana/` (reemplaza TU_USUARIO por el tuyo).
5. Desde el móvil, abre la URL y usa **Añadir a pantalla de inicio** para instalarla como app.

## Importante: almacenamiento y privacidad

- Los datos se guardan con `localStorage` **solo en el navegador que utilizas**. No se sincronizan entre dispositivos ni usuarios.
- Usa **Ajustes → Exportar copia** frecuentemente. La copia JSON puede importarse en otro navegador.
- Borrar datos del navegador puede borrar todos los registros si no hay copia.
- Cualquiera con la URL puede abrir la aplicación, pero no verá automáticamente tus registros locales; cada navegador mantiene su propio estado.
- No introduzcas datos sensibles o enlaces a documentos sensibles cuando la web no tenga control de acceso.
- Para editar y compartir una única base de datos entre dispositivos hace falta un backend: **no** es seguro habilitar INSERT/UPDATE/DELETE públicos en Supabase para una web sin login. Puede añadirse después una capa controlada de escritura o un acceso privado de administración.

## Datos iniciales

Se cargan el modelo, fecha y precio de compra y una ITV provisional para el **1 de febrero de 2027** (fecha concreta por confirmar). Se deja el kilometraje vacío para evitar asumir una cifra actual no verificada. Los mantenimientos e importes no se inventan ni se marcan como realizados.

## Compatibilidad

HTML, CSS y JavaScript puro, sin dependencias de npm. Funciona en GitHub Pages.
