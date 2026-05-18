Control de Stock — Legion S.A.
Aplicación PWA para control físico de inventario
---
¿Qué archivos hay?
`index.html` — La aplicación completa
`manifest.json` — Configuración para instalar como app
`sw.js` — Service Worker para funcionamiento offline
`README.md` — Este archivo
---
¿Cómo publicar la app en Internet? (Gratis)
La app necesita estar en un servidor web para que los celulares puedan acceder.
La opción más simple y GRATUITA es GitHub Pages o Netlify.
Opción A: Netlify (más fácil, 5 minutos)
Crear cuenta gratis en https://netlify.com
Entrar al dashboard → "Add new site" → "Deploy manually"
Arrastrar la CARPETA `stock-control` al área de deploy
Netlify genera una URL del tipo: `https://amazing-name-123.netlify.app`
¡Listo! Compartir esa URL con el equipo
Opción B: GitHub Pages
Crear cuenta en https://github.com
Crear repositorio nuevo (público)
Subir los 3 archivos (index.html, manifest.json, sw.js)
Ir a Settings → Pages → Source: main branch
URL quedará: `https://tuusuario.github.io/nombre-repo`
---
¿Cómo instalar la app en el celular?
Android (Chrome)
Abrir la URL de la app en Chrome
Tocar los 3 puntitos (menú) → "Agregar a pantalla de inicio"
Confirmar → La app aparece como ícono en el celular
iPhone (Safari)
Abrir la URL en Safari (NO Chrome en iPhone)
Tocar el botón compartir (cuadrado con flecha)
"Agregar a pantalla de inicio" → Agregar
La app aparece como ícono en el celular
---
Flujo de uso
Cargar PDF → Subir el informe "Saldos de Stock" exportado del sistema contable
Seleccionar materiales → Buscar y elegir los artículos a controlar
Conteo físico → Para cada artículo: ingresar cantidad contada y comentario
Reporte → Ver resumen de diferencias y exportar a Excel
---
Notas técnicas
El parseo del PDF funciona directamente en el navegador (sin servidor)
Los datos se mantienen en memoria durante la sesión
Varias personas pueden usar la app simultáneamente desde sus propios celulares
Para compartir resultados entre personas → cada uno exporta su Excel
Funciona sin internet una vez instalada (service worker)
---
Requerimientos del PDF
El PDF debe ser el informe "Saldos de Stock (Lote/Serie)" del sistema Legion/Crystal Reports.
Los artículos deben tener el formato: CÓDIGO (6 dígitos) + DESCRIPCIÓN + números de Entrada/Salida/Saldo.
