# Costo de Viaje V3

Versión preparada para GitHub Pages y uso como PWA en Android.

Incluye GPS de alta precisión, trazabilidad del recorrido GPS, ruta por calles mediante OSRM, origen/destino, tarifa configurable, costo, pausa, historial local, exportación JSON, recibo imprimible/Guardar como PDF, manifest y service worker.

## GitHub Pages
Sube el contenido de `app/` al repositorio y activa Pages desde `Settings > Pages > Deploy from a branch > main > /(root)`.

## Prueba local
`cd app && python3 -m http.server 8080` y abre `http://localhost:8080/Index.html`.

## Limitaciones
No existe GPS 100% preciso: la precisión depende del teléfono y entorno. La app usa `enableHighAccuracy`, muestra la precisión y descarta puntos fuera del límite configurado. El GPS en segundo plano tampoco está garantizado por navegadores móviles; para seguimiento profesional continuo se requiere una app Android nativa. El historial es local al navegador/dispositivo. OSRM y Nominatim públicos pueden tener límites de uso; para producción con tráfico alto conviene un proveedor o infraestructura propia.
