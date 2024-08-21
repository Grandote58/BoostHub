**Nombre del Proyecto:** *"Explorando el Sistema Solar"*

- **Objetivo Claro:** Introducir a los estudiantes a la estructura básica de una página web.
- **Objetivo Específico:** Crear una página web interactiva que muestre los planetas del sistema solar con información básica sobre cada uno.
- **Descripción:** En este proyecto, los estudiantes crearán una página web que presenta los planetas del sistema solar con imágenes y descripciones. Usarán HTML5 para estructurar la página, CSS para el diseño visual, y JavaScript para agregar interactividad, como hacer clic en un planeta para mostrar más información.

- Esquema General del Proyecto:
  - Secciones del Proyecto:
    1. **Encabezado:** Contendrá el título de la página "Explorando el Sistema Solar".
    2. **Vista del Sistema Solar:** Una sección que muestra todos los planetas con sus órbitas.
    3. **Panel de Información:** Una sección interactiva que muestra información detallada cuando se selecciona un planeta.

**Organización del Proyecto:**

- Creación de Carpetas:
  1. **Carpeta `css`:** Para colocar el archivo `styles.css` que contendrá los estilos del proyecto.
  2. **Carpeta `js`:** Para colocar el archivo `script.js` que manejará la interactividad del proyecto.
  3. **Carpeta `img`:** Para colocar las imágenes necesarias de los planetas.

**Estructura de Carpetas:**

```css
proyecto-sistema-solar/
├── css/
│   └── styles.css
├── img/
│   └── mercurio.png
│   └── venus.png
│   └── ... (imágenes de otros planetas)
├── js/
│   └── script.js
└── index.html
```



#### **2. Estructura HTML**

**Diseño de la Página:**

- Comienza creando la estructura básica de la página utilizando HTML5 y aprovechando la estructura de Bootstrap para el diseño responsivo.

- Código HTML:

  ```html
  <!DOCTYPE html>
  <html lang="es">
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Explorando el Sistema Solar</title>
      <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css">
      <link rel="stylesheet" href="css/styles.css">
  </head>
  <body>
      <!-- Encabezado -->
      <header class="bg-dark text-white text-center py-3">
          <h1>Explorando el Sistema Solar</h1>
      </header>
  
      <!-- Vista del Sistema Solar -->
      <div class="container my-5">
          <div id="sistema-solar" class="d-flex justify-content-center">
              <!-- Ejemplo: Orbita y Planeta -->
              <div class="orbita">
                  <img src="img/mercurio.png" alt="Mercurio" class="planeta" id="mercurio">
              </div>
              <!-- Repetir estructura para otros planetas -->
          </div>
      </div>
  
      <!-- Panel de Información -->
      <div class="container">
          <div id="panel-info" class="bg-light p-4 text-center">
              <h2>Información del Planeta</h2>
              <p>Selecciona un planeta para ver más detalles.</p>
          </div>
      </div>
  
      <script src="js/script.js"></script>
      <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
  </body>
  </html>
  ```

- Comentarios en el Código:

  - Asegúrate de que cada sección esté documentada para que los estudiantes entiendan su función:

  ```html
  <!-- Esta sección muestra los planetas del sistema solar -->
  <!-- Aquí se muestra la información detallada del planeta seleccionado -->
  ```

------

#### **3. Estilización con CSS**

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
      background-color: #0b3d91; /* Azul oscuro para el encabezado */
  }
  
  /* Estilo para el Sistema Solar */
  #sistema-solar {
      position: relative;
      width: 600px;
      height: 600px;
  }
  
  .orbita {
      position: absolute;
      width: 100%;
      height: 100%;
      border: 1px dashed #fff;
      border-radius: 50%;
  }
  
  .planeta {
      position: absolute;
      top: 0;
      left: 50%;
      width: 50px;
      height: 50px;
      margin-left: -25px;
  }
  
  /* Estilo para el Panel de Información */
  #panel-info {
      background-color: #fff;
      color: #000;
      border-radius: 10px;
  }
  ```

- Mejores Prácticas de CSS:

  - Modulariza el código utilizando clases reutilizables.
  - Usa Bootstrap para agilizar el diseño responsivo y aprovechar componentes predefinidos.

------

#### **4. Interactividad con JavaScript**

**Agregar Interactividad:**

- Crea un archivo `script.js` dentro de la carpeta `js` para manejar la interactividad.

- Código JavaScript:

  ```javascript
  // Información de los planetas
  const planetas = {
      mercurio: {
          nombre: "Mercurio",
          descripcion: "Es el planeta más cercano al Sol y el más pequeño del sistema solar.",
          imagen: "img/mercurio.png"
      },
      venus: {
          nombre: "Venus",
          descripcion: "Segundo planeta más cercano al Sol y el más parecido a la Tierra en tamaño.",
          imagen: "img/venus.png"
      },
      // Añadir datos para los demás planetas
  };
  
  // Función para mostrar información del planeta
  function mostrarInfo(planetaId) {
      const panel = document.getElementById('panel-info');
      const planeta = planetas[planetaId];
      panel.innerHTML = `
          <h2>${planeta.nombre}</h2>
          <img src="${planeta.imagen}" alt="${planeta.nombre}" style="width: 100px;">
          <p>${planeta.descripcion}</p>
      `;
  }
  
  // Añadir eventos a los planetas
  document.getElementById('mercurio').addEventListener('click', function() {
      mostrarInfo('mercurio');
  });
  
  document.getElementById('venus').addEventListener('click', function() {
      mostrarInfo('venus');
  });
  
  // Repetir para los demás planetas
  ```

- Mejores Prácticas de JavaScript:

  - Documenta cada función explicando claramente su propósito y cómo interactúa con los elementos HTML y CSS.
  - Usa `addEventListener` para manejar los eventos de forma modular y escalable.
  - Considera usar funciones anónimas para eventos simples y funciones nombradas para lógica más compleja.

------

#### **5. Documentación del Código**

**Proporciona Documentación Detallada:**

- Incluye comentarios y explicaciones claras en cada parte del código.

- Ejemplo de Comentarios:

  ```html
  <!-- Este botón permite al usuario seleccionar un planeta -->
  ```

  ```javascript
  // Función: Mostrar información del planeta seleccionado
  // Propósito: Actualiza el panel de información con datos del planeta seleccionado.
  // Interacción: Cambia el contenido del panel de información basado en el planeta clickeado.
  ```

- Importancia de la Documentación:

  - Los comentarios deben ayudar a los estudiantes a entender no solo qué hace el código, sino también por qué es necesario.




