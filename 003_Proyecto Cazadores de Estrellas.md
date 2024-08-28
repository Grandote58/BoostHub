# **Proyecto: Cazadores de Estrellas**

- **Objetivo Claro:** Enseñar los conceptos básicos de CSS para el diseño visual de páginas web.
- **Objetivo Específico:** Crear un mapa estelar interactivo donde los usuarios puedan aprender sobre diferentes constelaciones.
- **Descripción:** Los estudiantes diseñarán una página web que muestra un mapa estelar con diferentes constelaciones. Usarán CSS para diseñar las estrellas y las líneas que forman las constelaciones, y JavaScript para que al hacer clic en una constelación se muestre una descripción de la misma.

- Esquema General del Proyecto:
  - Secciones del Proyecto:
    1. **Encabezado:** Contendrá el título de la página "Cazadores de Estrellas".
    2. **Mapa Estelar:** Una sección que muestra las constelaciones en un cielo nocturno.
    3. **Panel de Información:** Una sección interactiva que muestra información sobre una constelación cuando se selecciona.

## 1.  **Organización del Proyecto:**

- Creación de Carpetas:

  1. **Carpeta `css`:** Para colocar el archivo `styles.css` que contendrá los estilos del proyecto.
  2. **Carpeta `js`:** Para colocar el archivo `script.js` que manejará la interactividad del proyecto.
  3. **Carpeta `img`:** Para colocar las imágenes necesarias de las constelaciones.

- **Estructura de Carpetas:**

  ```css
  proyecto-cazadores-estrellas/
  ├── css/
  │   └── styles.css
  ├── img/
  │   └── orion.png
  │   └── casiopea.png
  │   └── estrellas.jpg (fondo del mapa estelar)
  ├── js/
  │   └── script.js
  └── index.html
  ```

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
      <title>Cazadores de Estrellas</title>
      <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
      <link rel="stylesheet" href="/css/styles.css">
  </head>
  <body>
      <!-- Encabezado -->
      <header class="bg-dark text-white text-center py-3">
          <h1>Cazadores de Estrellas dd</h1>
      </header>
  
      <!-- Mapa Estelar -->
      <div class="container my-5">
          <div id="mapa-estelar" class="position-relative">
              <div class="constelacion" id="orion">
                  <img src="/IMG/16130649563132.jpg" alt="Orión" class="img-fluid">
                  <span class="nombre-constelacion">Orión</span>
              </div>
      
              <div class="constelacion" id="casiopea">
                  <img src="/IMG/orieon.jpg" alt="Casiopea" class="img-fluid">
                  <span class="nombre-constelacion">Casiopea</span>
              </div>
              <!-- Añadir más constelaciones con diferentes posiciones -->
          </div>
      </div>
  
      
  
      <!-- Panel de Información -->
      <div class="container">
          <div id="panel-info" class="bg-light p-4 text-center">
              <h2>Información de la Constelación</h2>
              <p>Selecciona una constelación para ver más detalles.</p>
          </div>
      </div>
  
      <script src="/javascript/script.js"></script>
      <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
  </body>
  </html>
  ```

- Comentarios en el Código:

  - Incluye comentarios en el código para que los estudiantes entiendan la estructura y función de cada sección:

  ```html
  <!-- Muestra las constelaciones en el mapa estelar -->
  <!-- Muestra información detallada de la constelación seleccionada -->
  ```

------

## **3. Estilización con CSS**

**Aplicación de Estilos:**

- Crea un archivo `styles.css` dentro de la carpeta `css` para definir el aspecto visual de la página.

- Código CSS:

  ```css
  /* Estilos Generales */
  body {
      background-color: #000; /* Fondo negro para simular el cielo nocturno */
      color: white;
      font-family: 'Arial', sans-serif;
  }
  
  /* Estilo para el Encabezado */
  header {
      background-color: #1a1a1a; /* Fondo oscuro para el encabezado */
  }
  
  /* Estilo para el Mapa Estelar */
  #mapa-estelar {
      height: 500px;
      background: url('../img/estrellas.jpg') no-repeat center center;
      background-size: cover;
      border: 2px solid #fff;
  }
  
  .constelacion {
      position: absolute;
  }
  
  /* Posiciones específicas de constelaciones */
  #orion {
      top: 100px; /* Equivalente a 20% de 500px */
      left: 150px; /* Equivalente a 30% de 500px */
  }
  
  #casiopea {
      top: 250px; /* Equivalente a 50% de 500px */
      left: 300px; /* Equivalente a 60% de 500px */
  }
  
  .img-fluid {
      width: 40px;
      height: 40px;
      object-fit: cover;
  }
  
  
  .nombre-constelacion {
      position: absolute;
      top: 10px;
      left: 10px;
      background-color: rgba(0, 0, 0, 0.5);
      color: #fff;
      padding: 5px;
      border-radius: 5px;
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
  - Usa Bootstrap para aprovechar su sistema de grillas y componentes predefinidos.

------

## **4. Interactividad con JavaScript**

**Agregar Interactividad:**

- Crea un archivo `script.js` dentro de la carpeta `js` para manejar la interactividad.

- Código JavaScript:

  ```javascript
  // Información de las constelaciones
  const constelaciones = {
      orion: {
          nombre: "Orión",
          descripcion: "Una de las constelaciones más reconocibles en el cielo nocturno, conocida como 'El Cazador'.",
          imagen: "img/orion.png"
      },
      casiopea: {
          nombre: "Casiopea",
          descripcion: "Esta constelación tiene la forma de una 'W' y es visible durante todo el año en el hemisferio norte.",
          imagen: "img/casiopea.png"
      },
      // Añadir datos para otras constelaciones
  };
  
  // Función para mostrar información de la constelación
  function mostrarInfo(constelacionId) {
      const panel = document.getElementById('panel-info');
      const constelacion = constelaciones[constelacionId];
      panel.innerHTML = `
          <h2>${constelacion.nombre}</h2>
          <img src="${constelacion.imagen}" alt="${constelacion.nombre}" style="width: 100px;">
          <p>${constelacion.descripcion}</p>
      `;
  }
  
  // Añadir eventos a las constelaciones
  document.getElementById('orion').addEventListener('click', function() {
      mostrarInfo('orion');
  });
  
  document.getElementById('casiopea').addEventListener('click', function() {
      mostrarInfo('casiopea');
  });
  
  // Repetir para otras constelaciones
  ```

- Mejores Prácticas de JavaScript:

  - Documenta cada función explicando claramente su propósito y cómo interactúa con los elementos HTML y CSS.
  - Usa `addEventListener` para manejar los eventos de forma modular y escalable.
  - Utiliza objetos para organizar la información de las constelaciones de manera clara y accesible.