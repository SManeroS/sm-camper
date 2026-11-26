# SM Camper 0.3 — El camino es parte del viaje

Actualización de la aplicación original 0.2, sin servicios externos obligatorios. Los siete archivos se publican en la raíz del mismo repositorio GitHub Pages; no hace falta reinstalar.

## Antes de actualizar
1. En la versión 0.2 del ordenador, Ajustes → Exportar datos. Guarda una copia con nombre identificable, por ejemplo SM_Camper_02_PC.json. Si hay datos propios en el móvil, haz otra copia allí.
2. Extrae el ZIP 0.3. En el repositorio sm-camper, Add file → Upload files. Selecciona los siete archivos extraídos (incluido style.css, no styles.css) y confirma Commit changes en main. No subas copias JSON personales.
3. En Actions verifica el despliegue. Abre la misma URL en el navegador habitual, actualiza (Ctrl+F5), y comprueba la versión 0.3 y los datos. En el móvil abre con conexión, cierra y vuelve a abrir si sigue la versión antigua. No borres el almacenamiento ni desinstales.

## Novedades
- Jornadas verdes, visitas/eventos azules, alojamiento ocre. Consulta independiente de edición; plegado individual y global.
- Turismo o camper por viaje; el perfil de la Renault Master permanece separado.
- Desplazamiento o estancia; tiempos manuales en minutos para conducción, comidas, descansos y duración de cada actividad. El total no suma de nuevo los minutos a pie; indica datos sin estimar. Una estancia no suma conducción; revisar avisos de incoherencia.
- Reordenación conserva fechas por defecto. Opción de reasignar fechas cronológicamente usando las fechas existentes, no inventa fechas nuevas. Las reservas/eventos viajan con la jornada: verificar sus fechas reales tras reordenar.
- Visitas/eventos: tipo, hora, duración, horario, precio y web. Alojamiento: hotel/apartamento/hostal, prioridad, reserva, servicios, teléfono, web. Los servicios y notas antiguas se mantienen.
- Dimensiones hasta 0.001 m, estado confirmado/aproximado/sin confirmar, crucero orientativo 90 km/h ajustable, combustible y distintivo ambiental. El campo antiguo maxSpeed se conserva internamente; no se interpreta como velocidad de crucero.
- TomTom Plan se abre como acceso externo general, no precarga ni transmite rutas ni usa API. Google Maps continúa con origen/destino y ubicaciones.
- Mismo localStorage (sm-camper-v1) y formato de copia JSON ampliado. Importar sustituye datos, no fusiona. No hay sincronización; exportar en PC y transferir/importar al móvil con precaución (respaldo previo).

## Pruebas hechas
Sintaxis app.js y sw.js y manifiesto válidos. Chromium, con HTML/CSS/JS originales de la nueva versión cargados inline y localStorage simulado: compatibilidad con datos 0.2, consulta y edición, desplegado, reordenación y avisos, cálculo de tiempos, evento, hotel, servicios, estancia de 0 km, guardado/recarga simulada, dimensiones al milímetro, exportación e importación con ejemplo 0.1. Sin errores JS en esos casos. Consulta y edición de ejemplo sin desbordamiento horizontal a 360 px. La navegación a un servidor de pruebas fue bloqueada por el entorno; no se ha verificado el service worker real, el funcionamiento offline, ni la instalación/actualización en GitHub Pages. Tampoco se verificó la apertura efectiva de TomTom ni el envío al navegador. No se ha modificado GitHub.

## Pruebas en dispositivos
1. Versión y conservación de viajes, visitas y ficha. 2. Consulta y plegado. 3. Editar y guardar. 4. Turismo, estancia y evento. 5. Tiempos y reordenación. 6. Alojamiento y reservas. 7. Abrir TomTom/Google Maps. 8. Copias de seguridad antiguas en ventana privada. 9. Offline en PC y móvil. 10. Actualización y uso móvil sin desplazamiento horizontal. Mantén el ZIP 0.2 y las copias anteriores hasta completar las pruebas.
