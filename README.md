# 🌐 Simulador de Flujo Máximo — Algoritmo de Ford-Fulkerson

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![SVG](https://img.shields.io/badge/SVG-Vector_Graphics-FFB13B?style=for-the-badge)

Una herramienta web interactiva y pedagógica desarrollada en **JavaScript Vanilla**, **HTML5** y **SVG** para modelar redes de transporte, configurar fuentes y sumideros, y resolver problemas de **Flujo Máximo** paso a paso mediante el **Algoritmo de Ford-Fulkerson**.

---

## 📌 Descripción del Proyecto

Este proyecto permite visualizar, experimentar y aprender de forma didáctica la teoría de redes y flujo máximo. El usuario puede diseñar un grafo dirigido o generarlo aleatoriamente, definir el nodo origen (fuente) y destino (sumidero), e interactuar directamente con la interfaz seleccionando caminos aumentantes y calculando sus cuellos de botella en tiempo real.

Ideal para estudiantes y docentes de **Investigación de Operaciones**, **Optimización**, **Teoría de Grafos** y **Estructuras de Datos y Algoritmos**.

---

## ✨ Características Principales

- **🔢 Configuración Dinámica de Vértices:**
  - Soporta entre 7 y 16 nodos distribuidos automáticamente en disposición circular.
- **🔗 Creación Flexible de Aristas:**
  - **Modo Manual:** Ingreso de nodo origen, nodo destino y capacidad/peso (1 - 9999).
  - **Modo Aleatorio:** Generación procedural de grafos dirigidos conectados.
  - **Soporte de Aristas Bidireccionales:** Curvatura automática mediante curvas Bézier cuadráticas para evitar solapamientos entre aristas opuestas.
- **🎯 Definición de Fuente y Sumidero:**
  - Validación de conectividad y detección preventiva de ciclos mediante DFS (*Depth-First Search*).
- **🕹️ Aprendizaje Interactivo del Algoritmo:**
  - Selección de caminos aumentantes haciendo clic directamente sobre los nodos en el SVG.
  - Validación de caminos válidos y detección del cuello de botella (capacidad residual mínima).
  - Desafío interactivo para ingresar el incremento de flujo correspondiente.
- **🎨 Semáforo Visual de Saturación:**
  - Código de colores dinámico en tiempo real según el ratio `flujo / capacidad`:
    - ⚫ **Negro:** Flujo nulo (`flujo = 0`).
    - 🟢 **Verde:** Saturación baja (`≤ 30%`).
    - 🟠 **Naranja:** Saturación media (`< 100%`).
    - 🔴 **Rojo:** Arista saturada (`100%`).
- **📊 Resumen y Finalización Automática:**
  - Algoritmo BFS (*Breadth-First Search*) de verificación para detectar cuándo ya no existen caminos residuales disponibles.
  - Reporte final con el valor del **Flujo Máximo total alcanzado** y el desglose ordenado de todos los caminos aumentantes empleados.
- **⚠️ Sistema de Alertas y Validaciones:**
  - Modales de advertencia amigables ante entradas inválidas, capacidades fuera de rango o nodos desconectados.

---

## 🚀 Cómo Ejecutar el Proyecto

Este proyecto no requiere gestores de paquetes, compilación ni instalación de dependencias externas.

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/TU_USUARIO/FlujoMaximoSecun.git
   ```
2. **Abrir el proyecto:**
   - Navega a la carpeta del proyecto y haz doble clic sobre el archivo `index.html`, o bien ábrelo directamente en tu navegador web preferido (Google Chrome, Firefox, Edge, Safari, etc.).
   - Alternativamente, si utilizas VS Code, puedes iniciarlo con la extensión **Live Server**.

---

## 📖 Guía de Uso Paso a Paso

1. **Configurar la Red:**
   - Define el número de vértices deseado (entre 7 y 16) y presiona **Aplicar**.
2. **Agregar Aristas y Capacidades:**
   - Presiona **Manual** para ingresar pares de nodos con sus pesos o haz clic en **Aleatorio** para una configuración automática.
3. **Establecer Fuente y Sumidero:**
   - Asigna los números de los nodos de origen (Fuente) y destino (Sumidero), y presiona **Aceptar**.
4. **Ejecutar Ford-Fulkerson:**
   - Haz clic secuencialmente sobre los nodos del grafo para trazar un camino aumentante desde la fuente hacia el sumidero.
   - Presiona **Verificar**.
   - Ingresa el cuello de botella (capacidad residual mínima) y haz clic en **Confirmar**.
   - Repite el proceso hasta que el simulador determine que se ha alcanzado el **Flujo Máximo**.

---

## 📂 Estructura de Archivos

```plaintext
FlujoMaximoSecun/
├── index.html       # Estructura de la interfaz de usuario, panel de control y lienzo SVG
├── style.css        # Hoja de estilos con diseño responsive, flexbox y estilos SVG
├── script.js       # Lógica del grafo, algoritmo de Ford-Fulkerson, BFS, DFS y eventos
└── README.md        # Documentación oficial del proyecto
```

---

## 🛠️ Tecnologías Empleadas

- **HTML5:** Semántica y maquetación de paneles.
- **CSS3:** Diseño con Flexbox, modal overlays y tipografías legibles.
- **JavaScript (ES6+):** Lógica matemática de redes, validación de ciclos, cálculo de flujo residual y manipulación del DOM.
- **SVG (Scalable Vector Graphics):** Renderizado vectorial de nodos, aristas dirigidas, marcadores de flechas dinámicos y textos de capacidades.

---

## 📄 Licencia

Este proyecto está bajo la Licencia **MIT**. Consulta el archivo `LICENSE` si deseas añadirlo, o úsalo libremente con fines educativos y personales.
