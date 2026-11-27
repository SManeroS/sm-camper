# SM Camper 0.3.1 — El camino es parte del viaje

Actualización de mantenimiento basada en los siete archivos del ZIP 0.3, sin cambiar el almacenamiento `sm-camper-v1` ni las unidades internas de las duraciones (minutos). No requiere reinstalación ni servicios nuevos.

## Cambios
- Conducción, comidas, descansos, duración a pie y duración total de cada visita/evento: campos separados de horas y minutos (0–59 minutos), con total automático y consulta en horas/minutos. Vacío sigue significando sin estimar; cero es un dato válido. La duración a pie no se suma de nuevo al total de la visita.
- Consulta: viajes previstos y realizados, jornadas plegadas inicialmente; viajes en curso, abiertas las jornadas de la fecha local actual (si no coincide ninguna, todas plegadas). Se mantienen los controles individuales y generales.
- Iconos y texto para servicios seleccionados de alojamientos. Notas antiguas intactas.
- Caché 0.3.1, archivos CSS/JS con versión, revisión de actualizaciones al recuperar conexión/visibilidad y aviso de recarga cuando cambia el controlador, sin recargar automáticamente ni descartar cambios de edición.
- Se acota la actualización de avisos de dificultad a las fichas editables.

## Actualización
1. Exporta una copia de seguridad de cada dispositivo con datos propios. Conserva copias antiguas y ZIP 0.3.
2. Extrae el ZIP 0.3.1; sube los siete archivos de la raíz al repositorio sm-camper mediante Add file → Upload files. Commit directly to main, Commit changes. No subas el ZIP ni las copias JSON personales.
3. En Actions comprueba que el nuevo despliegue acaba en verde. Abre la misma URL en Chrome, Ctrl+F5, verifica versión y datos. En el móvil abre conectado, cierra y vuelve a abrir si es necesario. Si aparece el aviso de actualización, guarda cambios y recarga. No desinstales ni borres datos.

## Verificación
Sintaxis de JS y manifiesto válidos. Pruebas en Chromium con HTML/CSS/JS cargados inline, almacenamiento simulado y datos de ejemplo 0.3: consulta plegada en previsto y realizado, apertura de jornada actual en curso, conversión y edición de duraciones, totales, estancia con cero, distinción vacío/cero, iconos, guardado compatible, importación de JSON de ejemplo, ancho 360 px en consulta/edición, sin errores JS en esos casos. Navegación al servidor local bloqueada por el entorno; service worker real, instalación, actualización real y uso offline pendientes de probar en dispositivos. GitHub no modificado.

## Pruebas pendientes antes del BEC
Confirmar versión y datos del PC; probar campos de tiempo, plegado e iconos; actualización móvil; transferencia PC→móvil mediante copia (importar sustituye todo, no combina; respaldar móvil antes); abrir la app móvil en modo avión y consultar el viaje. No hay sincronización automática ni cálculo TomTom API/GPX; los enlaces externos requieren conexión.
