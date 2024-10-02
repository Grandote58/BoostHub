# Proyecto: Exploradores de la Gravedad: Simulación de Caída Libre

Este proyecto tiene como objetivo simular de forma interactiva la caída libre de un objeto, permitiendo a los estudiantes modificar parámetros como la altura inicial, la gravedad y el coeficiente de fricción del objeto. A continuación se documenta el código y se explica paso a paso, además de los conceptos de física relacionados.

------

### **Estructura del Proyecto:**

El proyecto se organiza en las siguientes carpetas y archivos:

- `/css/estilos.css`: Contiene los estilos de la interfaz para la simulación.
- `/img`: Carpeta donde se encuentran las imágenes del fondo y del objeto.
- `/js/caida.js`: Archivo JavaScript que contiene la lógica de la simulación.
- `/index.html`: Estructura de la página web que incluye la interfaz de usuario y llama a los estilos y scripts.

### **Conceptos de Física Relacionados**

Este proyecto está basado en las leyes del movimiento bajo la gravedad, específicamente en la **caída libre**.

#### a. **Gravedad (g)**:

La aceleración causada por la gravedad terrestre es aproximadamente **9.81 m/s²**. Esta es la fuerza que hace que los objetos caigan hacia la Tierra.

#### b. **Tiempo de Caída** (𝑡):

El tiempo que tarda un objeto en caer desde una cierta altura depende de la gravedad y de la altura inicial del objeto. Se calcula con la fórmula:

 
$$
t = \sqrt{\frac{2h}{g}}t=g2h
$$


#### c. **Velocidad Final** (𝑣):

La velocidad que alcanza un objeto al final de su caída libre se calcula mediante:
$$
v = g ⋅ t
$$

#### d. **Distancia Recorrida** (𝑑):

La distancia que recorre un objeto durante su caída está dada por: 
$$
d = \frac{1}{2}  g  t ^ 2
$$

#### e. **Fricción**:

Este valor simula la resistencia que el objeto enfrenta durante la caída, similar a lo que ocurre con la resistencia del aire. Al aumentar la fricción, el objeto cae más lentamente.

#### f. **Coeficiente del Material**:

Cada material tiene una resistencia al movimiento que afecta la caída. Por ejemplo, un objeto que cae en el aire enfrenta más resistencia que uno que cae en el agua o el hierro.

### **Paso a Paso para Comprender el Proyecto**

1. **Introducción de Parámetros**: El usuario ingresa valores para la altura inicial, la gravedad, el coeficiente de fricción y selecciona el material del objeto.
2. **Inicio de la Simulación**: Se calcula el tiempo de caída, la velocidad y la distancia, y estos valores se actualizan en tiempo real mientras el objeto desciende.
3. **Visualización de Resultados**: El objeto cae dentro del contenedor, mostrando en pantalla los valores físicos calculados. Los estudiantes observan cómo factores como la fricción y el material del objeto afectan su caída.
4. **Reinicio**: El usuario puede reiniciar la simulación en cualquier momento para volver a ingresar nuevos parámetros.

### **HTML: Estructura de la interfaz**

El archivo `index.html` proporciona una estructura básica para la página:

#### a. Campos de Entrada:

Los estudiantes pueden ingresar los valores de:

- **Altura inicial (en metros)**: Define la altura desde la cual el objeto comenzará a caer.
- **Gravedad (en m/s²)**: Es la aceleración causada por la gravedad terrestre. Se usa el valor predeterminado de 9.81 m/s².
- **Material del objeto**: Permite seleccionar entre tres materiales (hierro, agua y aire), afectando el comportamiento de la caída por sus diferentes coeficientes de fricción.
- **Coeficiente de fricción**: Un valor entre 0 y 1 que simula la resistencia del objeto debido a la fricción.

#### b. Animación y Botones:

- El contenedor de la simulación muestra el objeto en caída dentro de un área de 800x350px.
- Hay botones para iniciar y reiniciar la simulación.

### Código HTML relevante:

```html
<body>
    <div class="container text-center mt-5">
        <h1>Exploradores de la Gravedad: Simulación de Caída Libre</h1>
        <p>Ingresa los parámetros para comenzar la simulación:</p>
</body>
```

- **`<body>`**: Inicia el cuerpo del documento donde se muestra el contenido visible de la página.
- **`<div class="container text-center mt-5">`**: Contenedor centralizado utilizando Bootstrap. `text-center` alinea el texto al centro, y `mt-5` agrega un margen superior.
- **`<h1>`**: Título principal de la página.
- **`<p>`**: Parágrafo explicativo sobre la funcionalidad del formulario.

------

```html
<div class="row mb-4">
    <div class="col-md-4">
        <input type="number" id="altura_inicial" class="form-control" placeholder="Altura inicial (m)" min="1">
    </div>
    <div class="col-md-4">
        <input type="number" id="gravedad" class="form-control" placeholder="Gravedad (m/s²)" value="9.81" min="1">
    </div>
    <div class="col-md-4">
        <select id="material" class="form-select">
            <option value="0.02">Hierro</option>
            <option value="0.1">Agua</option>
            <option value="0.47">Aire</option>
        </select>
        <label for="material">Selecciona el material</label>
    </div>
</div>
```

- `<div class="row mb-4">`

  : Inicia una fila de Bootstrap con un margen inferior de 4 (mb-4). Esta fila contiene tres columnas.

  - **`<div class="col-md-4">`**: Cada columna ocupa 4 de las 12 columnas disponibles en el diseño de Bootstrap para pantallas medianas (`md`).
  - **`<input type="number">`**: Campos de entrada de números. El campo de `altura_inicial` permite al usuario ingresar la altura desde la que cae el objeto, y el campo de `gravedad` permite modificar la gravedad (por defecto, 9.81 m/s²).
  - **`<select>`**: Lista desplegable donde el usuario selecciona el material del objeto, que influye en la fricción.
  - **`<label>`**: Etiqueta que describe el propósito de la lista desplegable, para mejorar la accesibilidad.

------

```html
<div class="row mb-4">
    <div class="col-md-6">
        <input type="number" id="friccion" class="form-control" placeholder="Coeficiente de fricción (0-1)" step="0.01" min="0" max="1">
    </div>
    <div class="col-md-6">
        <button class="btn btn-primary" onclick="iniciarSimulacion()">Iniciar Simulación</button>
        <button class="btn btn-danger" onclick="reiniciarSimulacion()">Reiniciar</button>
    </div>
</div>
```

- **Campo de entrada para el coeficiente de fricción**: Permite ingresar un valor decimal entre 0 y 1 que representa la fricción.
- Botones:
  - **Iniciar Simulación**: Llama a la función `iniciarSimulacion()` al hacer clic, que comienza la simulación.
  - **Reiniciar**: Llama a la función `reiniciarSimulacion()` al hacer clic, que reinicia los valores y la simulación.



```html
<div id="contenedor-caida" class="position-relative mx-auto">
    <img src="img/objeto.png" id="objeto" style="">
</div>
```

- **`<div id="contenedor-caida">`**: Contenedor donde ocurre la animación de la caída del objeto. La clase `position-relative` permite que el elemento hijo (el objeto) se posicione con respecto a este contenedor. `mx-auto` centra horizontalmente el contenedor.
- **`<img src="img/objeto.png">`**: Imagen que representa el objeto en caída. El `id="objeto"` permite manipular la posición y animación de este elemento desde JavaScript.

------

```html
<div class="mt-4">
    <p><strong>Tiempo de Caída:</strong> <span id="tiempo_caida">0</span> s</p>
    <p><strong>Velocidad Final:</strong> <span id="velocidad_final">0</span> m/s</p>
    <p><strong>Distancia Recorrida:</strong> <span id="distancia_recorrida">0</span> m</p>
</div>
```

- Información de salida

  : Estos elementos muestran los resultados de la simulación en tiempo real:

  - **Tiempo de Caída**: Muestra el tiempo que tarda el objeto en caer.
  - **Velocidad Final**: Muestra la velocidad del objeto al final de la caída.
  - **Distancia Recorrida**: Muestra la distancia total que recorrió el objeto.

Los valores iniciales son 0 y se actualizan en tiempo real durante la simulación gracias al JavaScript.

------

```html
<script src="/js/script.js"></script>
```

- **Vinculación del script**: Este archivo JavaScript (`script.js`) contiene la lógica para la simulación de caída libre. Maneja las interacciones de los botones y calcula los valores físicos basados en los parámetros ingresados.

### Solución Completa HTML

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exploradores de la Gravedad</title>
    <link rel="stylesheet" href="/css/estilo.css">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
    <div class="container text-center mt-5">
        <h1>Exploradores de la Gravedad: Simulación de Caída Libre</h1>
        <p>Ingresa los parámetros para comenzar la simulación:</p>
        
        <div class="row mb-4">
            <div class="col-md-4">
                <input type="number" id="altura_inicial" class="form-control" placeholder="Altura inicial (m)" min="1">
            </div>
            <div class="col-md-4">
                <input type="number" id="gravedad" class="form-control" placeholder="Gravedad (m/s²)" value="9.81" min="1">
            </div>
            <div class="col-md-4">
                <select id="material" class="form-select">
                    <option value="0.02">Hierro</option>
                    <option value="0.1">Agua</option>
                    <option value="0.47">Aire</option>
                </select>
                <label for="material">Selecciona el material</label>
            </div>
        </div>

        <div class="row mb-4">
            <div class="col-md-6">
                <input type="number" id="friccion" class="form-control" placeholder="Coeficiente de fricción (0-1)" step="0.01" min="0" max="1">
            </div>
            <div class="col-md-6">
                <button class="btn btn-primary" onclick="iniciarSimulacion()">Iniciar Simulación</button>
                <button class="btn btn-danger" onclick="reiniciarSimulacion()">Reiniciar</button>
            </div>
        </div>

        <div id="contenedor-caida" class="position-relative mx-auto" style="">
            <img src="img/objeto.png" id="objeto" style="">
        </div>

        <div class="mt-4">
            <p><strong>Tiempo de Caída:</strong> <span id="tiempo_caida">0</span> s</p>
            <p><strong>Velocidad Final:</strong> <span id="velocidad_final">0</span> m/s</p>
            <p><strong>Distancia Recorrida:</strong> <span id="distancia_recorrida">0</span> m</p>
        </div>
    </div>

    <script src="/js/script.js"></script>
</body>
</html>

```



### Código CSS relevante:

Este fragmento de código CSS define los estilos visuales para la simulación de caída libre de un objeto. A continuación, se documentan cada una de las secciones del código para una mejor comprensión.

------

```css
body {
    font-family: 'Arial', sans-serif;
}
```

- **`font-family: 'Arial', sans-serif;`**: Aplica la fuente **Arial** al texto de todo el documento. Si Arial no está disponible, utiliza la fuente genérica **sans-serif**. Esto asegura una apariencia limpia y legible.

------

```css
#contenedor-caida {
    width: 800px;   /* Ancho */
    height: 350px;  /* Altura */
    background-image: url('img/fondo.png'); /* Imagen de fondo */

    border: 1px solid #ccc;
    overflow: hidden;
    background-size: cover;
}
```

- `#contenedor-caida`

  : Es el contenedor principal donde ocurre la animación de la caída del objeto.

  - **`width: 800px;`**: El ancho del contenedor está establecido en 800 píxeles.
  - **`height: 350px;`**: La altura del contenedor es de 350 píxeles.
  - **`background-image: url('img/fondo.png');`**: Establece una imagen de fondo para el contenedor. En este caso, se utiliza una imagen ubicada en `img/fondo.png`.
  - **`border: 1px solid #ccc;`**: Agrega un borde gris claro (`#ccc`) de 1 píxel de grosor, para delinear el contenedor.
  - **`overflow: hidden;`**: Asegura que cualquier contenido (como el objeto) que se mueva fuera de los límites del contenedor no sea visible. Es importante para que el objeto "desaparezca" una vez salga del área visible.
  - **`background-size: cover;`**: Hace que la imagen de fondo cubra completamente el contenedor. Si la imagen es más pequeña, se escalará para ajustarse al tamaño del contenedor.

------

```css
#objeto {
    transition: top 0.1s linear;
    width: 40px;
    height: 40px;
    
    position: absolute;
    
    top: 20px;
    left: 200px;
}
```

- `#objeto`

  : Define el estilo para el objeto que cae dentro del contenedor.

  - **`transition: top 0.1s linear;`**: Aplica una transición suave a la propiedad `top`. Cada vez que se actualice la posición vertical del objeto, tomará 0.1 segundos en ajustarse de forma lineal, proporcionando una animación fluida durante la caída.
  - **`width: 40px;`** y **`height: 40px;`**: El objeto tiene un tamaño de 40 píxeles por 40 píxeles.
  - **`position: absolute;`**: El objeto se posiciona de manera absoluta dentro del contenedor, lo que permite moverlo mediante las propiedades `top` y `left`.
  - **`top: 20px;`**: Inicialmente, el objeto comienza a 20 píxeles desde la parte superior del contenedor.
  - **`left: 200px;`**: El objeto está posicionado a 200 píxeles desde el lado izquierdo del contenedor. Esto lo coloca en una posición personalizada dentro del área de caída.

### Solución Completa CSS

```css
body {
    font-family: 'Arial', sans-serif;
}

#contenedor-caida {

    width: 800px;   /* Ancho */
    height: 350px;  /* Altura */
    background-image: url('img/fondo.png'); /* Imagen */

    border: 1px solid #ccc;
    overflow: hidden;
    background-size: cover;
}

#objeto {
    transition: top 0.1s linear;
    width: 40px;
    height: 40px;
    
    position: absolute;
    
    top: 20px;
    left: 200px;
}

```



### Código JavaScript relevante:

La lógica para una simulación interactiva de caída libre. Los usuarios pueden ingresar valores de altura, gravedad, fricción y material del objeto. La simulación calcula en tiempo real el tiempo de caída, la velocidad y la distancia recorrida, actualizando la posición del objeto animado.

#### **Variables Globales**

```javascript
let altura_inicial = 0;
let gravedad = 9.81;
let tiempo = 0;
let velocidad = 0;
let distancia = 0;
let friccion = 0;
let coeficiente_material = 0;
let objeto = document.getElementById('objeto');
let intervaloSimulacion;
```

- **`altura_inicial`**: Almacena la altura desde la cual el objeto cae, ingresada por el usuario.
- **`gravedad`**: La aceleración debido a la gravedad, con un valor predeterminado de **9.81 m/s²** (gravedad terrestre).
- **`tiempo`**: Acumula el tiempo transcurrido durante la simulación.
- **`velocidad`**: Calcula la velocidad del objeto durante la caída.
- **`distancia`**: Almacena la distancia que ha recorrido el objeto en su caída.
- **`friccion`**: Representa el coeficiente de fricción ingresado por el usuario, que reduce la velocidad.
- **`coeficiente_material`**: Representa la resistencia adicional proporcionada por el material del objeto (aire, agua, hierro).
- **`objeto`**: Referencia al objeto en el HTML que está siendo animado durante la simulación.
- **`intervaloSimulacion`**: Variable que guarda el identificador del intervalo utilizado para actualizar la simulación en tiempo real.

------

#### **Función para Iniciar la Simulación**

```javascript
function iniciarSimulacion() {
    altura_inicial = parseFloat(document.getElementById('altura_inicial').value);
    gravedad = parseFloat(document.getElementById('gravedad').value);
    friccion = parseFloat(document.getElementById('friccion').value);
    coeficiente_material = parseFloat(document.getElementById('material').value);

    if (isNaN(altura_inicial) || isNaN(gravedad) || isNaN(friccion) || altura_inicial <= 0 || gravedad <= 0 || friccion < 0 || friccion > 1) {
        alert("Por favor, introduce valores válidos.");
        return;
    }

    // Cálculo del tiempo de caída
    tiempo = 0;
    distancia = 0;
    velocidad = 0;
    
    intervaloSimulacion = setInterval(actualizarSimulacion, 100);  // Actualiza cada 100ms
}
```

- Función `iniciarSimulacion`:

  ​       Esta función se ejecuta cuando el usuario hace clic en el botón "Iniciar Simulación".

  - **Entrada de valores**: Se toman los valores de altura, gravedad, fricción y material seleccionados por el usuario desde el formulario HTML y se convierten en números flotantes.
  - **Validación**: Verifica que los valores ingresados sean válidos. Si alguno es incorrecto (NaN o fuera de rango), se muestra un mensaje de alerta.
  - **Inicialización de variables**: Resetea el tiempo, distancia y velocidad para comenzar desde cero.
  - **Inicia la simulación**: La función `setInterval` llama a la función `actualizarSimulacion` cada 100 milisegundos, lo que actualiza la simulación en tiempo real.

------

#### **Función para Actualizar la Simulación**

```javascript
function actualizarSimulacion() {
    tiempo += 0.1;  // Incrementa el tiempo en cada intervalo de 0.1s
    velocidad = gravedad * tiempo * (1 - friccion - coeficiente_material);  // Aplicar fricción y coeficiente del material
    distancia = (0.5 * gravedad * Math.pow(tiempo, 2)) * (1 - friccion - coeficiente_material);
    
    if (distancia >= altura_inicial) {
        distancia = altura_inicial;
        clearInterval(intervaloSimulacion);  // Detener la simulación cuando el objeto llegue al suelo
    }
    
    // Actualizar los valores en la interfaz
    document.getElementById('tiempo_caida').innerText = tiempo.toFixed(2);
    document.getElementById('velocidad_final').innerText = velocidad.toFixed(2);
    document.getElementById('distancia_recorrida').innerText = distancia.toFixed(2);

    // Mover el objeto en la animación
    let posicionY = (distancia / altura_inicial) * (350 - 40);  // Ajustar según el contenedor
    objeto.style.top = posicionY + 'px';
}
```

- Función `actualizarSimulacion`

  : Esta función se ejecuta periódicamente (cada 100ms) para simular la caída del objeto y actualizar los valores en pantalla.

  - **Incrementa el tiempo**: Cada vez que se llama la función, el tiempo se incrementa en 0.1 segundos.

  - **Cálculo de la velocidad**: Se calcula utilizando la fórmula

     
    $$
    v = g \cdot t \cdot (1 - \text{friccion} - \text{coeficiente\_material})
    $$
    , que incluye los efectos de la fricción y el material.

  - **Cálculo de la distancia**: La distancia recorrida se calcula usando
    $$
    d = \frac{1}{2} \cdot g \cdot t^2 \cdot (1 - \text{friccion} - \text{coeficiente\_material})
    $$
    

  - **Detección del fin de la caída**: Si la distancia recorrida es mayor o igual a la altura inicial, el objeto ha llegado al suelo, y la simulación se detiene con `clearInterval()`.

  - **Actualización de valores**: Se actualizan los elementos HTML que muestran el tiempo de caída, la velocidad final y la distancia recorrida en pantalla.

  - **Animación del objeto**: Se ajusta la posición del objeto en el eje Y para simular su movimiento de caída dentro del contenedor.

------

#### **Función para Reiniciar la Simulación**

```javascript
function reiniciarSimulacion() {
    clearInterval(intervaloSimulacion);
    objeto.style.top = '20px';  // Resetea el objeto a su posición inicial
    document.getElementById('tiempo_caida').innerText = '0';
    document.getElementById('velocidad_final').innerText = '0';
    document.getElementById('distancia_recorrida').innerText = '0';
}
```

- Función `reiniciarSimulacion`

  : Esta función se ejecuta cuando el usuario hace clic en el botón "Reiniciar".

  - **Detener la simulación**: Se detiene el intervalo que actualiza la simulación utilizando `clearInterval()`.
  - **Restablecer la posición del objeto**: El objeto vuelve a su posición original al inicio de la simulación, en la parte superior del contenedor.
  - **Reiniciar los valores en pantalla**: Se resetean los valores de tiempo, velocidad y distancia mostrados al usuario a **0**.

### Solución Completa JavaScript

```javascript
// Variables globales
let altura_inicial = 0;
let gravedad = 9.81;
let tiempo = 0;
let velocidad = 0;
let distancia = 0;
let friccion = 0;
let coeficiente_material = 0;
let objeto = document.getElementById('objeto');
let intervaloSimulacion;

// Función para iniciar la simulación
function iniciarSimulacion() {
    altura_inicial = parseFloat(document.getElementById('altura_inicial').value);
    gravedad = parseFloat(document.getElementById('gravedad').value);
    friccion = parseFloat(document.getElementById('friccion').value);
    coeficiente_material = parseFloat(document.getElementById('material').value);

    if (isNaN(altura_inicial) || isNaN(gravedad) || isNaN(friccion) || altura_inicial <= 0 || gravedad <= 0 || friccion < 0 || friccion > 1) {
        alert("Por favor, introduce valores válidos.");
        return;
    }

    // Cálculo del tiempo de caída
    tiempo = 0;
    distancia = 0;
    velocidad = 0;
    
    intervaloSimulacion = setInterval(actualizarSimulacion, 100);  // Actualiza cada 100ms
}

function actualizarSimulacion() {
    tiempo += 0.1;  // Incrementa el tiempo en cada intervalo de 0.1s
    velocidad = gravedad * tiempo * (1 - friccion - coeficiente_material);  // Aplicar fricción y coeficiente del material
    distancia = (0.5 * gravedad * Math.pow(tiempo, 2)) * (1 - friccion - coeficiente_material);
    
    if (distancia >= altura_inicial) {
        distancia = altura_inicial;
        clearInterval(intervaloSimulacion);  // Detener la simulación cuando el objeto llegue al suelo
    }
    
    // Actualizar los valores en la interfaz
    document.getElementById('tiempo_caida').innerText = tiempo.toFixed(2);
    document.getElementById('velocidad_final').innerText = velocidad.toFixed(2);
    document.getElementById('distancia_recorrida').innerText = distancia.toFixed(2);

    // Mover el objeto en la animación
    let posicionY = (distancia / altura_inicial) * (350 - 40);  // Ajustar según el contenedor
    objeto.style.top = posicionY + 'px';
}

// Función para reiniciar la simulación
function reiniciarSimulacion() {
    clearInterval(intervaloSimulacion);
    objeto.style.top = '20px';  // Resetea el objeto a su posición inicial -- Aqui Cambio
    document.getElementById('tiempo_caida').innerText = '0';
    document.getElementById('velocidad_final').innerText = '0';
    document.getElementById('distancia_recorrida').innerText = '0';
}

```









