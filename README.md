# Pongpong
---

### **1. Estructura General**

El archivo es un documento HTML5 en español (`<html lang="es">`). Contiene la estructura básica de una web moderna, con el juego Pong entre dos inteligencias artificiales completamente integrado y todas las funcionalidades embebidas dentro del propio archivo (sin dependencias externas).

---

### **2. Encabezado (`<head>`)**

- **Codificación y viewport**  
  Incluye `<meta charset="UTF-8">` para soportar caracteres internacionales y `<meta name="viewport" ...>` para hacer la web responsive, adaptándose a móviles y tablets.

- **Título**  
  El título de la pestaña es “Pong AI vs AI Estratégico (Integrado)”.

- **Estilos CSS internos**  
  Todo el CSS está embebido dentro de una etiqueta `<style>`.  
  El CSS define:
    - Variables CSS para colores principales, acentuados, botones, colores de IA izquierda y derecha, fondos de pantallas, dimensiones, transiciones y accesibilidad.
    - Estilos para resetear márgenes y box-sizing en todos los elementos.
    - Estilos del `body` para centrar vertical y horizontal, fondo oscuro, y fuente sans-serif.
    - Soporte para modo oscuro y claro, cambiando variables para colores.
    - Encabezados y contenedores adaptables.
    - Estilo especial para el canvas del juego, con borde, sombra, esquinas redondeadas y responsividad.
    - Botones estilizados y accesibles, con transiciones y cambios de color al interactuar.
    - Etiquetas visuales para identificar a cada IA (izquierda/derecha) mediante color y posición.
    - Paneles modales para pantalla de inicio, pantalla de ganador y modo espectador, todos con estilos de transición y visibilidad.
    - Barras y paneles para controles y estadísticas.
    - Soporte responsive para dispositivos móviles y pantallas pequeñas.

---

### **3. Cuerpo (`<body>`)**

#### **3.1. Botón de cambio de tema**
- Un botón en la esquina superior derecha para alternar entre modo oscuro y claro.

#### **3.2. Encabezado del juego**
- Un `<header>` con un `<h1>` que muestra el título del juego.

#### **3.3. Área principal del juego (`<main>`)**
- **Etiquetas de IA**  
  Una barra superior identifica visualmente las dos IAs (izquierda/derecha) con colores y texto.

- **Canvas**  
  El área del juego es un `<canvas>` de 750x585 píxeles con atributos de accesibilidad (`tabindex`, `aria-label`, `role="img"`).

- **Controles del juego**  
  Un contenedor con botones:
    - Reiniciar partida
    - Pausar/Reanudar partida
    - Modo espectador (para ver repeticiones)
    - Exportar historial de partidas

- **Panel de estadísticas**  
  Un div muestra estadísticas en tiempo real: duración, rebotes, velocidad media de la bola.

#### **3.4. Pie de página**
- Un `<footer>` minimalista con el texto “Pong AI”.

---

### **4. Pantallas y paneles auxiliares**

#### **4.1. Pantalla de inicio**
- Modal que aparece al cargar el juego.
- Permite elegir dificultad (Fácil, Normal, Difícil, Personalizada).
- Si se selecciona “Personalizada”, aparecen inputs para ajustar velocidad de la bola, reacción y variabilidad de la IA.
- Botón para empezar el juego.
- Muestra estadísticas y el historial reciente de partidas.

#### **4.2. Pantalla de ganador**
- Modal que aparece al finalizar una partida.
- Muestra el ganador, el marcador final, estadísticas (duración, rebotes, velocidad media), y el historial reciente.
- Botón para jugar de nuevo.

#### **4.3. Panel de modo espectador**
- Modal para ver repeticiones de partidas guardadas.
- Incluye controles para cerrar el modo espectador.

#### **4.4. Barra de espectador**
- Panel flotante con controles para:
    - Ajustar la velocidad de la repetición.
    - Pausar/reanudar la repetición.
    - Seleccionar entre partidas previas guardadas.

---

### **5. Lógica JavaScript interna**

El JS está completamente embebido en una etiqueta `<script>`. El código:

- Controla la lógica principal del juego Pong:
    - Movimiento de la bola y las paletas (ambas controladas por IA).
    - Detección de colisiones y rebotes.
    - Sistema de puntuación y condiciones de victoria.
    - Control de pausa, reinicio y estado del juego.
    - Animaciones y transiciones visuales.
    - Adaptación de la dificultad y personalización de la IA.
- Implementa:
    - Guardado de estadísticas y repeticiones de partidas en localStorage.
    - Visualización de estadísticas y repeticiones, con modo espectador.
    - Exportación del historial a CSV.
    - Medidas de seguridad como sanitización de textos para evitar XSS.
    - Accesibilidad: soporte para teclado, roles ARIA, y foco automático.
    - Alternancia de temas (oscuro/claro) desde un botón.
- El JS no tiene sonidos ni recursos externos.
- No hay comentarios en el código, siguiendo tus instrucciones.

---

### **6. Seguridad**

- **Sanitización XSS:**  
  Todas las entradas de usuario y datos mostrados en historial y estadísticas son sanitizados antes de ser insertados en el DOM.
- **No recursos externos:**  
  No se cargan fuentes, imágenes, scripts ni hojas de estilo externas.
- **Control de foco y visibilidad:**  
  Cuando la pestaña pierde foco, el juego se pausa automáticamente.
- **Accesibilidad:**  
  Uso de ARIA, roles, y navegación por teclado para que el juego sea accesible.

---

### **7. Accesibilidad y experiencia**

- **Compatibilidad total con teclado (teclas para pausar y reiniciar).**
- **Paneles y modales accesibles y con roles adecuados.**
- **Contraste y fuentes adaptadas para mejor visualización.**
- **Interfaz adaptativa para dispositivos móviles.**

---

### **8. Funcionalidades avanzadas**

- **Dificultad y IA personalizable.**
- **Historial de partidas y repeticiones visualizables.**
- **Modo espectador para ver partidas anteriores o ajustar la velocidad de reproducción.**
- **Exportación de resultados en formato CSV.**
- **Transiciones visuales y animaciones.**
- **Cambio de tema visual (oscuro/claro).**

---

```
https://codezensual.github.io/pongpong/
