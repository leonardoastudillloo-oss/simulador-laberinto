# Simulador y Algoritmo de Resolución de Laberintos

Este repositorio contiene un proyecto interactivo desarrollado en **HTML5, CSS3 y JavaScript** que permite simular y comparar el comportamiento de distintos algoritmos (secuencias de instrucciones) para navegar por un laberinto hasta encontrar la salida.

---

## 📌 1. Fundamentos Teóricos del Algoritmo

Diseñar un algoritmo para recorrer un laberinto implica planificar cómo un personaje, avatar o robot puede navegar de manera eficiente desde la entrada hasta la salida.

### **Paso a paso en lenguaje natural:**
1. **Inicio:** Comienza en la entrada/punto de partida del laberinto.
2. **Exploración:** Observa las direcciones posibles en las que puedes moverte (*izquierda, derecha, arriba, abajo*).
3. **Selección:** Elige una dirección para moverte (por ejemplo, comenzar girando a la derecha).
4. **Desplazamiento:** Avanza los pasos indicados en la dirección elegida.
5. **Evaluación de estado:**
   - ¿Llegaste a la salida? **¡Proceso finalizado!**
   - ¿No has llegado? Regresa al paso 2 y repite la exploración desde la nueva ubicación.

### **Reglas de optimización y control de errores:**
* **Marcado de casillas:** Registrar el rastro visitado para evitar entrar en bucles infinitos.
* **Manejo de callejones sin salida (*Backtracking*):** Si te encuentras con una pared o un obstáculo, retrocede a la casilla o intersección anterior y elige una nueva dirección.
* **Criterio de decisión fijo:** Usar reglas consistentes en los cruces (por ejemplo, seguir siempre la pared izquierda/derecha).

---

## 🛠️ 2. Comparativa de Secuencias Ejecutables

El simulador cuenta con 3 algoritmos precargados para analizar su desempeño dentro del mapa:

### 🟢 Algoritmo Correcto (Completado)
Llega exitosamente al punto de finalización siguiendo la ruta sin colisiones.
* **Secuencia de pasos:**
  1. Avanzar 2 pasos ➡️ Girar a la derecha
  2. Avanzar 2 pasos ➡️ Girar a la derecha
  3. Avanzar 1 paso ➡️ Girar a la izquierda
  4. Avanzar 2 pasos ➡️ Girar a la derecha
  5. Avanzar 2 pasos ➡️ Girar a la derecha
  6. Avanzar 3 pasos ➡️ Girar a la izquierda
  7. Avanzar 2 pasos ➡️ Girar a la izquierda
  8. Avanzar 2 pasos ➡️ Girar a la derecha
  9. Avanzar 2 pasos ➡️ Girar a la derecha
  10. Avanzar 2 pasos ➡️ Girar a la izquierda
  11. Avanzar 2 pasos ➡️ Girar a la derecha
  12. Avanzar 2 pasos ➡️ Girar a la izquierda
  13. Avanzar 3 pasos ➡️ Girar a la derecha
  14. Avanzar 3 pasos ➡️ Girar a la derecha
  15. Avanzar 3 pasos ➡️ Girar a la izquierda
  16. Avanzar 2 pasos ➡️ Girar a la izquierda
  17. Avanzar 2 pasos ➡️ **Llegada / Final**

### 🔴 Algoritmo Incorrecto 1 (Colisión / Ruta Corta)
Termina en colisión al intentar avanzar por un camino bloqueado.
* **Secuencia de pasos:**
  - Avanzar 2 pasos ➡️ Girar a la derecha ➡️ Avanzar 6 pasos ➡️ Girar a la izquierda ➡️ Avanzar 3 pasos ➡️ Girar a la derecha ➡️ Avanzar 2 pasos ➡️ Girar a la izquierda ➡️ Avanzar 5 pasos ➡️ Girar a la derecha ➡️ Avanzar 3 pasos ➡️ Girar a la izquierda ➡️ Avanzar 4 pasos ➡️ **Bloqueo / Colisión**.

### 🟡 Algoritmo Incorrecto 2 (Desvío / Callejón sin salida)
Toma un desvío hacia la sección inferior del tablero y no logra alcanzar la meta.
* **Secuencia de pasos:**
  - Secuencia de 32 pasos alternando giros a la izquierda/derecha que dirigen al avatar hacia una casilla sin salida en la parte inferior del mapa.

---

## 💻 3. Tecnologías Utilizadas

* **HTML5:** Estructura del maquetado y los botones de control.
* **CSS3:** Sistema de rejilla (`Grid`), diseño responsivo y estilos visuales de trayectorias.
* **JavaScript (Vanilla):** Control del bucle de animación, interpretación de comandos y validación de límites.

---

## 🚀 4. Cómo Ejecutar este Proyecto

1. Clona el repositorio o descarga el código fuente:
   ```bash
   git clone [https://github.com/TU_USUARIO/TU_REPOSITORIO.git](https://github.com/TU_USUARIO/TU_REPOSITORIO.git)
