# Sitio Web — vitrina pública de Los Pinos

App interna de **Triplay y Molduras "Los Pinos"**, pero de naturaleza distinta a las demás: no
corre en `DELL-SERVIDOR`, vive publicada en **GitHub Pages** bajo el dominio propio
**triplaylospinos.com** (comprado en Namecheap, cuenta `vargasge`, ago-2026).

Estado: **v0**, mockup validado con el usuario. Nació de una plática sobre analizar proveedores
de ferretería (Polanco vs Ferre-Herrajes del Norte) que terminó en "quiero mi propia página
como la de Ferre-Herrajes del Norte".

## Qué es

**Vitrina, NO e-commerce.** Catálogo navegable (buscador + categorías con foto) que manda al
cliente a WhatsApp o a visitar la tienda física — la tienda física sigue siendo el punto de
venta, aquí no hay carrito ni cobro en línea. Decisión explícita del usuario.

- `index.html` — página principal: buscador (filtro visual simple, sin backend), categorías con
  foto (Triplay y Tableros, Melamina y MDF, Molduras, Marcos a medida, Herrajes, Tornillería y
  Fijación, Acabados, Corte Láser), sección de confianza, sección "Visítanos" (dirección/horario/
  teléfono — hoy con placeholders entre corchetes, falta contenido real).
- `dia-de-muertos.html` — página de temporada para Corte Láser (calaveritas con nombre, letreros
  para altar), pensada como destino de un anuncio pagado (Meta/Google Ads) o como sección normal
  del sitio. Mismo sistema de diseño que `index.html`.
- Sin `Servidor.ps1`, sin backend, sin datos de SAE todavía — es HTML/CSS/JS estático plano, sin
  build. Cuando se conecte a SAE en el futuro: **solo artículos con existencia o movimiento
  reciente**, nunca el catálogo crudo completo (regla explícita del usuario, mismo criterio que
  VentaRapida/Ferreteria).

## Cómo se publica

No hay servidor propio ni puerto — GitHub Pages sirve los archivos estáticos del repo
directamente. Para ver cambios en internet: editar el `.html`, commit y push a `main`; Pages
lo republica solo (1-2 min).

`CNAME` (contiene `triplaylospinos.com`) le dice a GitHub Pages qué dominio propio usar. El DNS
del dominio (en Namecheap) apunta al hosting de GitHub — ver [[sitio-web-los-pinos-estilo]] en
memoria para los valores exactos que se configuraron y su fecha.

## Pendiente

1. Contenido real: número de WhatsApp, dirección de la tienda, horario — hoy son placeholders.
2. Fotos reales de piezas de Corte Láser para la sección "Ejemplos" de `dia-de-muertos.html`.
3. Confirmar que el DNS en Namecheap ya propagó y `https://triplaylospinos.com` carga solo.
4. A futuro: conectar categorías a datos reales de SAE (con el filtro de movimiento ya acordado).
