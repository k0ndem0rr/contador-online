# Contador Online

Una app de contadores minimalista para el navegador, pensada para vivir en GitHub Pages. Sin backend, sin cuenta, sin dependencias externas, todo en un único `index.html`.

## Qué hace

Permite crear múltiples **contadores** independientes. Cada contador tiene un nombre y un conjunto de opciones, cada una con su propio botón grande. Un toque = +1. Los datos se guardan automáticamente en el dispositivo.

### Funcionalidades

- **Múltiples contadores** — gestión desde la barra lateral, con el total visible de un vistazo
- **N opciones por contador** — las defines tú al crear el contador
- **Botones grandes** — toda la tarjeta es el botón, con animación de ripple y pop al contar
- **Colores automáticos** según el número de opciones:
  - 1 opción → verde lima
  - 2 opciones → lima + complementario (violeta)
  - 3 opciones → triángulo cromático (lima, azul, naranja)
  - 4+ → escala de verdes
- **Resumen en tiempo real** — barras de progreso con porcentajes, o gráfico de tarta tipo donut
- **Modo edición** — botón ✎ Editar que activa controles inline: renombrar contador, renombrar opciones, editar número directamente, eliminar opciones, añadir nuevas, resetear contadores
- **Compartir por URL** — genera un enlace con los datos de el contador codificados; quien lo abra la importa automáticamente
- **Modo oscuro** — toggle en la barra superior, se recuerda entre sesiones
- **Memoria local** — todo se guarda en `localStorage`, nada sale del dispositivo

## Uso de la app

### Crear un contador

Pulsa **+ Nuevo contador** en la barra lateral, ponle nombre y define las opciones que quieras contar. Mínimo una.

### Contar

Pulsa cualquier parte de la tarjeta de color para sumar 1. El número hace pop y aparece un ripple.

### Editar

Pulsa **✎ Editar** junto al nombre del contador. Esto activa:

- **✎** al lado del título → renombrar el contador
- **✎** al lado del nombre de cada opción → renombrar la opción
- **Click en el número** → editarlo directamente (solo dígitos, Enter para confirmar)
- **✕** en la esquina de cada tarjeta → eliminar esa opción
- **Tarjeta +** al final del grid → añadir una nueva opción
- **Resetear contadores** → pone todos a 0

Pulsa **✓ Listo** para salir del modo edición.

### Compartir

Pulsa **⬡ Compartir** — se copia al portapapeles una URL con los datos del contador. Quien la abra verá el contador importado en su dispositivo con el nombre original + *(importado)*. Es una instantánea, no sincronización en tiempo real.

## Tecnología

- HTML + CSS + JS vanilla — cero dependencias
- `localStorage` para persistencia
- Canvas API para el gráfico de tarta
- Fuentes: [Playfair Display](https://fonts.google.com/specimen/Playfair+Display), [DM Sans](https://fonts.google.com/specimen/DM+Sans), [DM Mono](https://fonts.google.com/specimen/DM+Mono) vía Google Fonts
