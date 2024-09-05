# Recordar Concepto !.

**`document.getElementById`** es un método en JavaScript que se utiliza para seleccionar y manipular un elemento específico dentro de un documento HTML basado en su atributo `id`. Es una de las formas más comunes de acceder a elementos del DOM (Document Object Model) para poder modificarlos o interactuar con ellos.

## ¿Cómo funciona?

Cuando una página web se carga en el navegador, se crea una representación estructurada del documento HTML llamada **DOM**. Cada elemento HTML (como `div`, `input`, `p`, etc.) se convierte en un nodo en esta estructura. Cada nodo puede tener un `id` único que permite identificarlo de manera específica dentro del documento.

El método `document.getElementById` toma como argumento una cadena que coincide con el valor del atributo `id` de un elemento en el DOM. Si encuentra un elemento con ese `id`, devuelve una referencia al nodo HTML correspondiente; si no lo encuentra, devuelve `null`.

## Sintaxis

```javascript
var elemento = document.getElementById('id_del_elemento');
```

- **`id_del_elemento`**: Es el identificador único que se le asigna al elemento HTML que deseas seleccionar.
- **`elemento`**: Es la referencia al elemento del DOM que puedes manipular (como cambiar su contenido, estilos, agregarle eventos, etc.).

## Ejemplo simple

En este ejemplo, vamos a cambiar el texto de un párrafo utilizando `document.getElementById`.

**HTML:**

```html
<p id="miParrafo">Este es un párrafo inicial.</p>
<button onclick="cambiarTexto()">Cambiar texto</button>
```

**JavaScript:**

```javascript
function cambiarTexto() {
    var parrafo = document.getElementById('miParrafo');
    parrafo.textContent = "El texto ha sido cambiado!";
}
```

## Funcionamiento paso a paso:

1. **Buscar el elemento**: `document.getElementById('miParrafo')` busca el elemento en el DOM que tiene el `id` "miParrafo".
2. **Manipular el elemento**: Con la referencia al elemento, se modifica su propiedad `textContent` para cambiar el texto dentro del párrafo.

## Limitaciones

- **Único para el documento**: Un `id` debe ser único en el documento HTML. Si hay múltiples elementos con el mismo `id`, `getElementById` solo devolverá el primero que encuentre.
- **Solo por `id`**: Este método solo selecciona elementos por su atributo `id`, no funciona con clases u otros selectores.

En resumen, `document.getElementById` es una herramienta fundamental en JavaScript para acceder de forma directa a los elementos de una página y realizar modificaciones o interacciones dinámicas con ellos.

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
      <link rel="stylesheet" href="/css/styles.css">
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
                  <button type="button" id="reiniciar-simulacion" class="btn btn-secondary">Reiniciar Simulación</button>
              </form>
              
          </div>
      </div>
  
      <!-- Simulación -->
      <div class="container">
          <div id="simulacion" class="position-relative">
             
              <!-- Imagen de la nave espacial -->
              <img src="/IMG/nave.jpg" alt="Nave Espacial" id="nave" class="position-absolute nave">
          </div>
      </div>
  
      <!-- Panel de Resultados -->
      <div class="container">
          <div id="panel-resultados" class="bg-light p-4 text-center mt-4">
              <h2>Resultados de la Simulación</h2>
              <p id="resultado">Ajusta los parámetros y presiona "Iniciar Simulación" para ver el resultado.</p>
          </div>
      </div>
  
      <script src="/javascript/jsnew.js"></script>
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
      width: 1300px;
      height: 500px;
      background: url('/IMG/marte.png') no-repeat center center;   
      background-size: cover;
      border: 2px solid #fff;
      position: relative;
  }
  
  
  
  /* Estilo para el Panel de Resultados */
  #panel-resultados {
      background-color: #fff;
      color: #000;
      border-radius: 10px;
  }
  
  /* Estilos para la simulación */
  .marte {
      width: 1200px;
      height: 500px;
  }
  
  .nave {
      width: 60px;
      height: 60px;
      top: 50%;  /* Centrar verticalmente la nave dentro de Marte */
      left: 50%; /* Centrar horizontalmente la nave dentro de Marte */
      transform: translate(-50%, -50%);
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
  // Función para actualizar la visualización de los valores
  // Esta función actualiza en tiempo real los valores visualizados de la velocidad e inclinación
  // conforme el usuario los modifica en los controles de entrada.
  function actualizarValores() {
      // Se obtienen los valores actuales de los campos de velocidad e inclinación.
      const velocidad = document.getElementById('velocidad').value;
      const inclinacion = document.getElementById('inclinacion').value;
      
      // Se actualizan los elementos en pantalla para mostrar los valores seleccionados.
      document.getElementById('velocidad-display').textContent = velocidad;
      document.getElementById('inclinacion-display').textContent = inclinacion;
  }
  
  // Función para iniciar la simulación
  // Esta función se encarga de ejecutar la lógica que determina si la nave espacial ha aterrizado 
  // correctamente en Marte según los valores de velocidad e inclinación proporcionados.
  function iniciarSimulacion() {
      // Se obtienen los valores actuales de los controles de velocidad e inclinación.
      const velocidad = document.getElementById('velocidad').value;
      const inclinacion = document.getElementById('inclinacion').value;
      
      // Elemento donde se mostrará el resultado de la simulación (éxito o fallo).
      const resultado = document.getElementById('resultado');
      
      // Elemento que representa la nave espacial en la simulación.
      const nave = document.getElementById('nave');
  
      // Lógica simple para determinar si el aterrizaje es exitoso:
      // El aterrizaje es exitoso si la velocidad es menor o igual a 50 y la inclinación está entre -10 y 10.
      const exito = velocidad <= 50 && inclinacion >= -10 && inclinacion <= 10;
  
      // Se actualiza el texto del resultado dependiendo de si el aterrizaje fue exitoso o fallido.
      resultado.textContent = exito 
          ? "¡Éxito! La nave ha aterrizado correctamente en Marte." 
          : "Fallido. La nave se estrelló en Marte.";
  
      // Cambia el color del texto del resultado para hacer más claro el éxito o el fallo.
      resultado.style.color = exito ? "green" : "red";
  
      // Se anima la posición de la nave en la pantalla simulando el aterrizaje.
      // Si el aterrizaje es exitoso, la nave desciende al 80% de la pantalla; si falla, desciende al 95%.
      nave.style.top = exito ? "80%" : "95%";
      
      // La transición visual se aplica durante 2 segundos con una aceleración/desaceleración suave.
      nave.style.transition = "top 2s ease-in-out";
  }
  
  // Función para reiniciar la simulación
  // Esta función restablece los valores de velocidad e inclinación a sus estados iniciales
  // y coloca la nave en su posición de partida, permitiendo que el usuario reinicie la simulación.
  function reiniciarSimulacion() {
      // Se restablecen los valores de los controles de entrada de velocidad e inclinación.
      document.getElementById('velocidad').value = 50;
      document.getElementById('inclinacion').value = 0;
      
      // Se actualizan los valores mostrados en pantalla a los valores predeterminados.
      actualizarValores();
      
      // Se coloca la nave en su posición inicial en la parte superior de la pantalla.
      const nave = document.getElementById('nave');
      nave.style.top = "20%";  // Asume que "20%" es la posición inicial de la nave.
      
      // Se elimina la transición para que el restablecimiento de la posición sea instantáneo.
      nave.style.transition = "none";
  
      // Se imprime un mensaje en la consola del navegador indicando que la simulación se ha reiniciado.
      console.log('Simulación reiniciada');
  }
  
  // Añadir eventos
  // Estos eventos permiten que el usuario interactúe con la simulación y actualice los valores en tiempo real.
  
  // Cuando el usuario cambia los valores de velocidad o inclinación, se actualizan las visualizaciones.
  document.getElementById('velocidad').addEventListener('input', actualizarValores);
  document.getElementById('inclinacion').addEventListener('input', actualizarValores);
  
  // Cuando el usuario hace clic en el botón para iniciar la simulación, se ejecuta la lógica de aterrizaje.
  document.getElementById('iniciar-simulacion').addEventListener('click', iniciarSimulacion);
  
  // Cuando el usuario hace clic en el botón de reinicio, la simulación se restablece a su estado inicial.
  document.getElementById('reiniciar-simulacion').addEventListener('click', reiniciarSimulacion);
  
  ```
  
  
  
  ## Mejores Prácticas de JavaScript:
  
  - Documenta cada función explicando claramente su propósito y cómo interactúa con los elementos HTML y CSS.
  - Usa `addEventListener` para manejar los eventos de forma modular y escalable.
  - Utiliza transiciones CSS junto con JavaScript para crear efectos visuales suaves.