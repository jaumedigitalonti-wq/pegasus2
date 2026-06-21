# PEGASUS Centro Deportivo — Web

Dos páginas estáticas (HTML + Tailwind por CDN + JavaScript vanilla, sin necesidad de instalar nada):

- `index.html` — Landing del gimnasio (programas, instalaciones, planes, contacto con ficha estilo Google Maps).
- `tienda.html` — Tienda de suplementos con carrito de la compra funcional (añadir, cambiar cantidad, filtrar por categoría, checkout simulado).
- `images/` — Las dos fotos reales del gimnasio que me pasaste, usadas en la sección "Nuestras instalaciones".

## Cómo verlo en local

No hace falta backend ni `npm install`. Dos opciones:

**Opción A — doble clic**
Abre `index.html` directamente con el navegador.

**Opción B — servidor local (recomendado, evita pequeños problemas de rutas)**
Desde esta carpeta, en una terminal:

```bash
python3 -m http.server 8000
```

y abre `http://localhost:8000` en el navegador.

## Qué es totalmente funcional ahora mismo

- Carrito de la compra (persistente con `localStorage`): añadir productos, subir/bajar cantidad, ver total, vaciar al finalizar.
- Filtros de categoría y "cargar más productos" en la tienda.
- Formulario de checkout con validación y confirmación de pedido (número de pedido simulado).
- Botón "Guardar", "Compartir" y "Enviar al teléfono" en la ficha de contacto (con feedback real en pantalla).
- Estado "Abierto/Cerrado" calculado con la hora real del visitante (abre a las 7:00).
- Menú móvil funcional en ambas páginas.

## Importante sobre los pagos

El checkout de la tienda simula el proceso de compra (valida el formulario, genera un número de pedido y vacía el carrito), pero **no está conectado a ningún banco ni pasarela de pago real**. Para cobrar de verdad necesitarás integrar una pasarela como Stripe o Redsys, lo cual requiere un servidor/backend además de esta parte visual. Dime si quieres que lo preparemos.
