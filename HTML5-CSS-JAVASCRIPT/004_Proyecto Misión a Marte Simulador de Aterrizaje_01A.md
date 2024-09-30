Proyecto **"Recrea la Misión a Marte: Simulador de Aterrizaje"**

**Introducción**: 

Este proyecto tiene como objetivo simular el aterrizaje de una nave en Marte, permitiendo que los estudiantes controlen la velocidad y el frenado en tiempo real utilizando tecnologías web como **HTML5, CSS, JavaScript** y **Bootstrap**. Aprenderán los fundamentos de estas tecnologías mientras desarrollan una simulación interactiva.

**Esquema General del Proyecto:** 

Los estudiantes crearán una simulación donde se muestra una nave espacial que aterriza en Marte con controles interactivos. La estructura del proyecto se organizará de la siguiente manera:

- `css/`: Contendrá la hoja de estilos CSS.
- `js/`: Guardará los archivos JavaScript que agregan interactividad.
- `images/`: Carpeta para la imagen del planeta Marte y la nave espacial.
- `index.html`: La página principal del simulador.

**Preparación del Entorno:**

1. Crear la estructura de carpetas mencionada.
2. Crear los archivos básicos:
   - `index.html`
   - `style.css`
   - `script.js`
3. Abrir el proyecto en **Visual Studio Code** o cualquier editor de texto.
4. Asegúrate de tener las imágenes de Marte y la nave espacial listas en la carpeta `images/`.



### **Funcionamiento General:**

- **Aumentar Velocidad:** Usa el botón "Aumentar Velocidad" para incrementar la velocidad de caída.
- **Frenar:** Usa el botón "Frenar" para reducir la velocidad.
- **Mover Izquierda/Derecha:** Usa los botones correspondientes para ajustar la posición horizontal de la nave.
- **Reiniciar:** El botón "Reiniciar" devolverá la nave a su altura y velocidad iniciales.
- **Aterrizaje:** Para un aterrizaje exitoso, la nave debe estar en **0 km/h** cuando esté entre **3 y 15 metros** de altura.



### **2. Estructura HTML**

**Diseño de la Página HTML:** Usaremos **HTML5** para definir la estructura de la página. Esta debe incluir elementos como el encabezado, el contenedor para la imagen del planeta, y los controles para la velocidad y fricción.

**Ejemplo del Código HTML:**

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Simulador de Aterrizaje en Marte</title>
    <link rel="stylesheet" href="css/style.css" />
    <link
      rel="stylesheet"
      href="https://stackpath.bootstrapcdn.com/bootstrap/5.0.0/css/bootstrap.min.css"
    />
  </head>
  <body>
    <!-- Encabezado -->
    <header class="text-center bg-dark text-white p-4">
      <h1>Simulador de Aterrizaje en Marte</h1>
    </header>

    <!-- Área de simulación -->
    <main class="container mt-4">
      <div
        id="mars-landing"
        class="border"
        style="
          width: 1000px;
          height: 400px;
          background-image: url('images/mars.jpg');
          background-size: cover;
        "
      >
        <img
          id="nave"
          src="images/spacecraft.png"
          alt="Nave espacial"
          style="
            width: 40px;
            height: 40px;
            position: absolute;
            top: 50px;
            left: 50%;
          "
        />
        <img
          id="imagen-buen-aterrizaje"
          src="images/good-landing.png"
          alt="Buen aterrizaje"
          style="display: none; width: 40px; height: 40px; position: absolute"
        />
        <img
          id="imagen-mal-aterrizaje"
          src="images/bad-landing.png"
          alt="Mal aterrizaje"
          style="display: none; width: 40px; height: 40px; position: absolute"
        />
      </div>

      <!-- Controles de velocidad, fricción, movimiento y reinicio -->
      <div class="text-center mt-4">
        <button id="aumentar-velocidad" class="btn btn-success">
          Aumentar Velocidad
        </button>
        <button id="frenar" class="btn btn-warning">Frenar</button>
        <button id="mover-izquierda" class="btn btn-primary">
          Mover Izquierda
        </button>
        <button id="mover-derecha" class="btn btn-primary">
          Mover Derecha
        </button>
        <button id="reiniciar" class="btn btn-danger">Reiniciar</button>
      </div>

      <!-- Indicadores de velocidad, altura y tiempo -->
      <div class="text-center mt-3">
        <p>Velocidad Actual: <span id="velocidad">5</span> km/h</p>
        <p>Altura Actual: <span id="altura">400</span> metros</p>
        <p>Tiempo de Caída: <span id="tiempo">0</span> segundos</p>
        <p>
          <strong
            >Velocidad requerida para aterrizar: 0 km/h, a 20 metros de
            altura</strong
          >
        </p>
      </div>
    </main>

    <script src="js/script.js"></script>
  </body>
</html>

```



### **3. Estilización con CSS**

**Estilos en CSS:** El CSS será responsable de darle un aspecto atractivo a la simulación. Aquí se aplicarán estilos básicos a los botones, al fondo de Marte, y a la nave espacial.

**Ejemplo del Código CSS:**

```css
/* style.css */

/* Estilos básicos */
body {
  font-family: Arial, sans-serif;
  background-color: #0d0d2d;
  color: white;
}

/* Encabezado */
header {
  background-color: #20232a;
  padding: 20px;
}

/* Contenedor de la simulación */
#mars-landing {
  margin: 0 auto;
  position: relative;
  overflow: hidden;
}

/* Estilo de la nave espacial */
#nave {
  position: absolute;
  top: 50px;
  left: calc(50% - 20px);
}

/* Imágenes de aterrizaje */
#imagen-buen-aterrizaje,
#imagen-mal-aterrizaje {
  position: absolute;
  left: calc(50% - 20px);
}

/* Botones */
button {
  margin: 10px;
}

```

**Mejores Prácticas de CSS:**

1. Reutiliza clases y evita repetir el código.
2. Mantén el código organizado usando comentarios para separar las secciones.
3. Usa nombres de clases significativos para que el código sea más fácil de entender.

### **4. Interactividad con JavaScript**

**Añadiendo Interactividad con JavaScript:** La funcionalidad principal se añadirá con **JavaScript**. Se creará un sistema para controlar la velocidad de la nave espacial y su fricción al aterrizar. Además, se mostrarán mensajes emergentes cuando se active el control de fricción.

**Ejemplo del Código JavaScript:**

```javascript
// Variables globales
let velocidad = 5; // Velocidad inicial en km/h
let altura = 400; // Altura inicial en metros
let tiempo = 0; // Tiempo en segundos
let gravedad = 3.7; // Gravedad en Marte (m/s^2)
let frenadoActivo = false;
let posicionHorizontal = 50; // Posición horizontal inicial
let cayendo = true; // Controla si la nave está cayendo

// Elementos del DOM
const velocidadElemento = document.getElementById("velocidad");
const alturaElemento = document.getElementById("altura");
const tiempoElemento = document.getElementById("tiempo");
const nave = document.getElementById("nave");
const imagenBuenAterrizaje = document.getElementById("imagen-buen-aterrizaje");
const imagenMalAterrizaje = document.getElementById("imagen-mal-aterrizaje");
const botonAumentarVelocidad = document.getElementById("aumentar-velocidad");
const botonFrenar = document.getElementById("frenar");
const botonIzquierda = document.getElementById("mover-izquierda");
const botonDerecha = document.getElementById("mover-derecha");
const botonReiniciar = document.getElementById("reiniciar");

// Función para aumentar la velocidad
botonAumentarVelocidad.addEventListener("click", () => {
  velocidad += 10;
  actualizarVelocidadAltura();
});

// Función para frenar la nave
botonFrenar.addEventListener("click", () => {
  if (!frenadoActivo) {
    alert("¡Frenando el aterrizaje!");
    frenadoActivo = true;
    velocidad = Math.max(velocidad - 3, 0); // Reduce la velocidad en 3 km/h
    actualizarVelocidadAltura();
    setTimeout(() => {
      frenadoActivo = false;
    }, 3000); // El frenado dura 3 segundos
  }
});

// Función para mover la nave a la izquierda
botonIzquierda.addEventListener("click", () => {
  posicionHorizontal = Math.max(0, posicionHorizontal - 5);
  nave.style.left = `${posicionHorizontal}%`;
});

// Función para mover la nave a la derecha
botonDerecha.addEventListener("click", () => {
  posicionHorizontal = Math.min(100, posicionHorizontal + 5);
  nave.style.left = `${posicionHorizontal}%`;
});

// Función para reiniciar la simulación
botonReiniciar.addEventListener("click", () => {
  reiniciarSimulacion();
});

// Simulación de caída libre utilizando la fórmula física
let intervaloCaida = setInterval(() => {
  if (cayendo) {
    tiempo += 0.1; // Incrementar el tiempo
    actualizarVelocidadAltura();
  }
}, 100);

// Función para actualizar velocidad y altura usando la fórmula de caída libre
function actualizarVelocidadAltura() {
  // Fórmula de caída libre: h = h0 - 0.5 * g * t^2
  if (altura > 0) {
    altura = Math.max(0, 400 - 0.5 * gravedad * Math.pow(tiempo, 2)); // Actualizar la altura según la fórmula
  }

  // Mostrar la velocidad y altura en la interfaz
  velocidadElemento.innerText = velocidad.toFixed(1);
  alturaElemento.innerText = altura.toFixed(1);
  tiempoElemento.innerText = tiempo.toFixed(1);

  // Mover la nave en la pantalla
  moverNave();

  // Comprobar condiciones de aterrizaje o fallo
  if (altura <= 20 && velocidad > 0) {
    // Mal aterrizaje
    alert("¡Aterrizaje fallido! Velocidad mayor a 0.");
    mostrarMalAterrizaje();
  } else if (altura <= 20 && velocidad === 0) {
    // Buen aterrizaje
    alert("¡Aterrizaje exitoso en Marte!");
    mostrarBuenAterrizaje();
  }
}

// Mover la nave en la pantalla
function moverNave() {
  nave.style.top = `${Math.max(0, 400 - altura)}px`;
}

// Función para reiniciar la simulación
function reiniciarSimulacion() {
  velocidad = 5; // Restablecer velocidad
  altura = 400; // Restablecer altura
  tiempo = 0; // Restablecer tiempo
  posicionHorizontal = 50; // Restablecer posición horizontal
  cayendo = true; // Habilitar la caída de nuevo
  nave.style.left = "50%"; // Restablecer posición de la nave
  nave.style.top = "50px"; // Restablecer la altura de la nave
  nave.style.display = "block"; // Mostrar la nave
  imagenBuenAterrizaje.style.display = "none"; // Ocultar la imagen de buen aterrizaje
  imagenMalAterrizaje.style.display = "none"; // Ocultar la imagen de mal aterrizaje
  clearInterval(intervaloCaida); // Detener el intervalo anterior
  intervaloCaida = setInterval(() => {
    if (cayendo) {
      tiempo += 0.1;
      actualizarVelocidadAltura();
    }
  }, 100);
}

// Función para mostrar imagen de buen aterrizaje
function mostrarBuenAterrizaje() {
  nave.style.display = "none"; // Ocultar la nave
  imagenBuenAterrizaje.style.top = nave.style.top;
  imagenBuenAterrizaje.style.left = nave.style.left;
  imagenBuenAterrizaje.style.display = "block"; // Mostrar imagen de buen aterrizaje
  cayendo = false; // Detener la caída
}

// Función para mostrar imagen de mal aterrizaje
function mostrarMalAterrizaje() {
  nave.style.display = "none"; // Ocultar la nave
  imagenMalAterrizaje.style.top = nave.style.top;
  imagenMalAterrizaje.style.left = nave.style.left;
  imagenMalAterrizaje.style.display = "block"; // Mostrar imagen de mal aterrizaje
  cayendo = false; // Detener la caída
}

```



### **Documentación de la Función de Caída Libre**

```javascript
/**
 * Función de caída libre que simula el descenso de la nave utilizando
 * la fórmula física de caída libre: h = h0 - (1/2) * g * t^2.
 * Esta fórmula calcula la altura a partir de la altura inicial (h0 = 500 metros)
 * considerando la gravedad de Marte (g = 3.7 m/s^2) y el tiempo de caída (t).
 * La función actualiza continuamente la velocidad y altura de la nave.
 */
```

### **Mejoras Implementadas:**

1. **Frenado Mejorado:** El frenado ahora reduce la velocidad en **3 km/h** cada vez que se presiona el botón de frenado.

2. Fórmula de Caída Libre Física:

    La altura de la nave ahora se calcula utilizando la fórmula física de caída libre:

   - $$
     h = h_0 - \frac{1}{2} g t^2
     $$

     

   - **g** es la gravedad en Marte (3.7 m/s²).

3. **Visualización del Tiempo de Caída:** Se muestra en pantalla el tiempo que ha pasado desde el inicio de la caída.

4. **Simulación Realista:** La nave comienza a caer con aceleración debida a la gravedad y debe reducir la velocidad a **0 km/h** para aterrizar con éxito entre **3 y 15 metros**.



## Mensaje Inspirador

Cada línea de código que escribes es un paso más hacia el descubrimiento y la creación. Este simulador no solo te enseña a programar, sino también a soñar en grande. Tal como los ingenieros que diseñan misiones espaciales, tú estás aprendiendo a dar vida a ideas increíbles. No hay límites cuando combinas la tecnología con tu creatividad. ¡El espacio y la programación están llenos de infinitas posibilidades!



