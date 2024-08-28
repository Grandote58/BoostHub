# Proyecto: Misión a Marte: Simulador de Aterrizaje

- **Objetivo Claro:** Introducir conceptos básicos de JavaScript para crear interactividad.
- **Objetivo Específico:** Crear un simulador simple donde los usuarios puedan intentar aterrizar una nave en Marte.
- **Descripción:** Los estudiantes desarrollarán una página web que simula el aterrizaje de una nave en Marte. Usarán HTML5 para la estructura, CSS para el diseño del simulador, y JavaScript para controlar la lógica del aterrizaje y mostrar mensajes dependiendo del resultado.

- Esquema General del Proyecto:
  - Secciones del Proyecto:
    1. **Encabezado:** Contendrá el título de la página "Misión a Marte: Simulador de Aterrizaje".
    2. **Panel de Control:** Una sección donde los usuarios pueden ajustar los parámetros de aterrizaje.
    3. **Simulación:** Una sección que muestra visualmente la simulación del aterrizaje en Marte.
    4. **Panel de Resultados:** Una sección que muestra el resultado del aterrizaje, indicando si fue exitoso o fallido.

## 1. **Organización del Proyecto:**

- Creación de Carpetas:
  1. **Carpeta `css`:** Para colocar el archivo `styles.css` que contendrá los estilos del proyecto.
  2. **Carpeta `js`:** Para colocar el archivo `script.js` que manejará la interactividad del proyecto.
  3. **Carpeta `img`:** Para colocar las imágenes necesarias, como la nave espacial y el fondo de Marte.

**Estructura de Carpetas:**

```css
proyecto-mision-marte/
├── css/
│   └── styles.css
├── img/
│   └── marte.png
│   └── nave.png
├── js/
│   └── script.js
└── index.html
```

- 1. 

------

## **2. Estructura HTML**

**Diseño de la Página:**

- Crea la estructura básica de la página utilizando HTML5 y Bootstrap para un diseño limpio y responsivo.

- Código HTML:

  ```html
  <!DOCTYPE html>
  <html lang="es">
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Misión a Marte: Simulador de Aterrizaje</title>
      <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css">
      <link rel="stylesheet" href="css/styles.css">
  </head>
  <body>
      <!-- Encabezado -->
      <header class="bg-dark text-white text-center py-3">
          <h1>Misión a Marte: Simulador de Aterrizaje</h1>
      </header>
  
      <!-- Panel de Control -->
      <div class="container my-5">
          <div id="panel-control" class="text-center">
              <h2>Panel de Control</h2>
              <form id="control-form">
                  <div class="mb-3">
                      <label for="velocidad" class="form-label">Velocidad de Descenso (m/s)</label>
                      <input type="range" class="form-range" id="velocidad" min="1" max="100" value="50">
                      <span id="velocidad-display">50</span> m/s
                  </div>
                  <div class="mb-3">
                      <label for="inclinacion" class="form-label">Inclinación (grados)</label>
                      <input type="range" class="form-range" id="inclinacion" min="-90" max="90" value="0">
                      <span id="inclinacion-display">0</span>°
                  </div>
                  <button type="button" id="iniciar-simulacion" class="btn btn-primary">Iniciar Simulación</button>
              </form>
          </div>
      </div>
  
      <!-- Simulación -->
      <div class="container">
          <div id="simulacion" class="position-relative">
              <img src="img/marte.png" alt="Marte" class="img-fluid w-100">
              <img src="img/nave.png" alt="Nave Espacial" id="nave" class="position-absolute">
          </div>
      </div>
  
      <!-- Panel de Resultados -->
      <div class="container">
          <div id="panel-resultados" class="bg-light p-4 text-center mt-4">
              <h2>Resultados de la Simulación</h2>
              <p id="resultado">Ajusta los parámetros y presiona "Iniciar Simulación" para ver el resultado.</p>
          </div>
      </div>
  
      <script src="js/script.js"></script>
      <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
  </body>
  </html>
  ```

- Comentarios en el Código:

  - Incluye comentarios en el código para que los estudiantes entiendan la estructura y función de cada sección:

  ```html
  <!-- Sección donde los usuarios ajustan los parámetros de aterrizaje -->
  <!-- Muestra la simulación visual del aterrizaje en Marte -->
  <!-- Muestra los resultados de la simulación -->
  ```

------

## **3. Estilización con CSS**

**Aplicación de Estilos:**

- Crea un archivo `styles.css` dentro de la carpeta `css` para definir el aspecto visual de la página.

- Código CSS:

  ```css
  /* Estilos Generales */
  body {
      background-color: #000; /* Fondo negro para simular el espacio */
      color: white;
      font-family: 'Arial', sans-serif;
  }
  
  /* Estilo para el Encabezado */
  header {
      background-color: #1a1a1a; /* Fondo oscuro para el encabezado */
  }
  
  /* Estilo para el Panel de Control */
  #panel-control {
      background-color: #333;
      border-radius: 10px;
      padding: 20px;
  }
  
  #panel-control input[type="range"] {
      width: 100%;
  }
  
  /* Estilo para la Simulación */
  #simulacion {
      height: 500px;
      background: url('../img/marte.png') no-repeat center center;
      background-size: cover;
      border: 2px solid #fff;
      position: relative;
  }
  
  #nave {
      width: 100px;
      left: 50%;
      transform: translateX(-50%);
  }
  
  /* Estilo para el Panel de Resultados */
  #panel-resultados {
      background-color: #fff;
      color: #000;
      border-radius: 10px;
  }
  ```

- Mejores Prácticas de CSS:

  - Modulariza el código utilizando clases reutilizables.
  - Usa Bootstrap para aprovechar su sistema de grillas y componentes predefinidos.

------

## **4. Interactividad con JavaScript**

**Agregar Interactividad:**

- Crea un archivo `script.js` dentro de la carpeta `js` para manejar la interactividad.

- Código JavaScript:

  ```javascript
  // Actualizar los valores de los rangos en tiempo real
  document.getElementById('velocidad').addEventListener('input', function() {
      document.getElementById('velocidad-display').textContent = this.value;
  });
  
  document.getElementById('inclinacion').addEventListener('input', function() {
      document.getElementById('inclinacion-display').textContent = this.value;
  });
  
  // Función para iniciar la simulación
  document.getElementById('iniciar-simulacion').addEventListener('click', function() {
      const velocidad = document.getElementById('velocidad').value;
      const inclinacion = document.getElementById('inclinacion').value;
      const resultado = document.getElementById('resultado');
      let exito;
  
      // Lógica simple para determinar el éxito del aterrizaje
      if (velocidad <= 50 && inclinacion >= -10 && inclinacion <= 10) {
          exito = true;
          resultado.textContent = "¡Éxito! La nave ha aterrizado correctamente en Marte.";
          resultado.style.color = "green";
      } else {
          exito = false;
          resultado.textContent = "Fallido. La nave se estrelló en Marte.";
          resultado.style.color = "red";
      }
  
      // Mostrar la nave descendiendo
      const nave = document.getElementById('nave');
      nave.style.top = exito ? "80%" : "95%";
      nave.style.transition = "top 2s ease-in-out";
  });
  ```

  

  ## Mejores Prácticas de JavaScript:

  - Documenta cada función explicando claramente su propósito y cómo interactúa con los elementos HTML y CSS.
  - Usa `addEventListener` para manejar los eventos de forma modular y escalable.
  - Utiliza transiciones CSS junto con JavaScript para crear efectos visuales suaves.