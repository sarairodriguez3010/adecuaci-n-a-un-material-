# Notas de Trabajo, Ideas Didácticas y Pensamientos del Proyecto "Animales"

Este documento compila todas las ideas, análisis, adaptaciones pedagógicas y recomendaciones de infraestructura que desarrollamos durante nuestra sesión de trabajo.

---

## 1. Análisis del Repositorio Original
El repositorio original **Gabriela-Eliza/Animales.** es un entorno de pruebas educativas que contiene:
* **`README.md`**: Un archivo inicial con la descripción *"Pruevas."*.
* **`juego_sonidos_animales.zip`**: Un empaquetado comprimido con el código y recursos locales del juego.
* **`Juego_Sonidos_Animales.html`**: Un interactivo web infantil que enseña onomatopeyas de 6 animales (vaca 🐮, pollito 🐥, perro 🐶, gato 🐱, gallo 🐓 y caballo 🐴).

---

## 2. Recomendaciones de Inclusión (Alumna de Lento Aprendizaje)
Para integrar a una alumna con ritmos de aprendizaje pausados, se establecieron las siguientes bases pedagógicas y de diseño de experiencia de usuario (UX):
* **Foco visual absoluto:** Eliminar distracciones visuales del tablero mientras un elemento está activo, ayudándole a concentrar sus canales visuales de forma selectiva.
* **Procesamiento de audio simplificado:** Reducir la velocidad y estructurar fonéticamente los sonidos para evitar sobrecarga auditiva y favorecer la decodificación silábica del lenguaje.
* **Andamiaje multisensorial:** Usar tarjetas físicas de papel idénticas a los emojis interactivos para que la alumna asocie el concepto concreto (tarjeta física) con la representación abstracta (pantalla).
* **Aprendizaje Kinestésico:** Involucrar a todo el grupo en la imitación física de movimientos y sonidos del animal respectivo para favorecer la memoria corporal.

---

## 3. Adaptaciones Implementadas en el Código
Modificamos el archivo principal `Juego_Sonidos_Animales.html` con las siguientes mejoras de inclusión:

### A. Foco de Atención Visual (CSS & JS)
* Al hacer clic en un animal, las tarjetas restantes reciben las propiedades:
  * `opacity: 0.25;` (Se atenúan).
  * `filter: grayscale(80%) blur(1px);` (Pierden color y nitidez).
  * `transform: scale(0.92);` (Se encogen levemente).
  * `pointer-events: none;` (Se deshabilitan clics en otros animales mientras dure el sonido).
* La tarjeta del animal activo destaca con las propiedades:
  * `transform: scale(1.08);` (Aumenta de tamaño).
  * Sombra verde pronunciada (`box-shadow`) y borde verde brillante.

### B. Refuerzo Verbal Pausado y Silabeado (JS en Text-To-Speech)
Cuando el sonido real falla, el navegador activa la síntesis de voz en español (`es-MX`) con:
* Velocidad reducida a `0.75` (Ritmo pausado).
* Una frase que deletrea el nombre del animal de forma silábica:
  * *"Esta es la... va... ca... y hace... ¡Muuuu, muuuu!"*
  * *"Este es el... pe... rro... y hace... ¡Guau, guau!"*

---

## 4. Opciones y Ruta de Trabajo en GitHub

* **Para Ti:** 
  1. Realizar un **Fork** del repositorio original para guardar estas adaptaciones personalizadas en tu propia cuenta.
  2. Descargar el código en formato **ZIP** o clonarlo mediante git para usarlo localmente en el aula sin internet.
* **Para la Autora (Gabriela-Eliza):**
  * Puede activar **GitHub Pages** para generar un enlace público de modo que puedas abrir el juego desde cualquier tableta o celular del grupo de preescolar sin necesidad de instalar archivos.
