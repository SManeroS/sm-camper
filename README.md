# SM Camper 0.2
El camino es parte del viaje.

## Actualizar desde 0.1
1. En cada dispositivo, abrir SM Camper 0.1 > Ajustes > Exportar datos y guardar la copia JSON en un sitio seguro. Las copias de PC y móvil pueden ser distintas.
2. Descomprimir este ZIP. En el repositorio existente `sm-camper`, rama `main`, usar Add file > Upload files. Subir los siete archivos sueltos a la raíz, no el ZIP ni una carpeta. Confirmar el commit. No crear otro repositorio.
3. Comprobar en Actions que pages build and deployment termina en verde. Abrir la misma dirección https://smaneros.github.io/sm-camper/. Cerrar todas las ventanas de la aplicación y volver a abrir; en PC recargar con Ctrl+F5 si sigue apareciendo 0.1. En móvil cerrar aplicación y Chrome y volver a abrir. El service worker usa una caché nueva; puede necesitar una segunda apertura para actualizar.
4. Comprobar que se ve 0.2 y que los viajes, etapas y ficha permanecen. No desinstalar ni borrar datos del navegador. Si falta información, no introducir cambios hasta comprobar la dirección y la copia; Ajustes > Importar copia sustituye los datos del dispositivo, no los combina.

## Novedades
- Fechas en español en el listado; los controles de fecha dependen del navegador. Duración inclusiva y noches según fechas de inicio y fin.
- Suma de kilómetros introducidos manualmente; las etapas sin distancia se señalan.
- Reordenar etapas con Subir/Bajar; no modifica sus fechas ni recalcula rutas.
- Fichas independientes de visitas y pernoctas, manteniendo los campos antiguos de notas. La dificultad se introduce a mano; avisa si está fuera de la preferencia, no elimina visitas ni busca recomendaciones.
- Enlaces a Google Maps de trayectos y ubicaciones. Google Maps no garantiza rutas aptas para dimensiones o peso de la camper. Verificar restricciones independientemente. Requiere conexión para consultar mapas.
- Ficha técnica ampliada: matrícula opcional, MMA, consumo, combustible, agua y velocidad. No se deducen datos técnicos ni legales.
- La clave local `sm-camper-v1` permanece intacta y se admiten copias JSON 0.1. Exportar antes de actualizar y no volver a editar con 0.1 una vez se hayan añadido campos nuevos.
- Sin sincronización automática, búsqueda turística, IA ni cálculo automático de distancias. La aplicación se puede consultar offline tras cargar los recursos mediante el service worker; no incluye mapas offline.

## Prueba recomendada
Abrir Portugal 2027 (debe conservar 2 etapas). Verificar fechas y total de 640 km si los datos originales eran 475 y 165. Editar: añadir una visita y una pernocta, cambiar orden, guardar, cerrar y abrir. Confirmar datos y ficha, exportar; probar importación en ventana privada. Comprobar el móvil y modo sin conexión después de una primera carga online.
