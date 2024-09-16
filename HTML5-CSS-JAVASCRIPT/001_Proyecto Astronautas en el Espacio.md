# Conceptos Iniciales

## **`document.getElementById`:**

Cuando creamos una página web con HTML, podemos agregarle diferentes elementos como textos, imágenes, botones, etc. El **`document.getElementById`** es una manera de decirle a la computadora: **"Quiero encontrar y controlar uno de esos elementos que tienen un ID especial".**

Un **ID** es como el nombre único que le damos a un elemento, y con **`document.getElementById`**, podemos decirle a nuestra página que busque ese nombre y cambie algo sobre el elemento (como el color o el texto).

### **¿Cómo funciona?**

1. Le das un nombre (ID) a un elemento en tu página.
2. Usas **`document.getElementById('nombreID')`** para encontrar ese elemento.
3. Luego, puedes hacer que algo cambie en ese elemento (por ejemplo, cambiar el color, el texto o esconderlo).

### Ejemplo 1: Cambiar el texto de un párrafo

Cuando haces clic en el botón, el texto del párrafo cambia.

```html
<!DOCTYPE html>
<html>
<body>

<p id="miParrafo">Este es el texto original.</p>
<button onclick="cambiarTexto()">Cambiar texto</button>

<script>
function cambiarTexto() {
    document.getElementById("miParrafo").innerHTML = "¡El texto ha cambiado!";
}
</script>

</body>
</html>
```



### Ejemplo 2: Cambiar el color de un título

Al hacer clic en el botón, el color del título cambia a rojo.

```html
<!DOCTYPE html>
<html>
<body>

<h1 id="miTitulo">¡Hola!</h1>
<button onclick="cambiarColor()">Cambiar color</button>

<script>
function cambiarColor() {
    document.getElementById("miTitulo").style.color = "red";
}
</script>

</body>
</html>
```



### Ejemplo 3: Ocultar una imagen

Al hacer clic en el botón, la imagen desaparece.

```html
<!DOCTYPE html>
<html>
<body>

<img id="miImagen" src="imagen.jpg" width="300">
<button onclick="ocultarImagen()">Ocultar imagen</button>

<script>
function ocultarImagen() {
    document.getElementById("miImagen").style.display = "none";
}
</script>

</body>
</html>
```

Estos ejemplos muestran cómo usar **`document.getElementById`** para encontrar elementos en la página y cambiar cosas como el texto, el color o incluso ocultarlos. ¡Es una herramienta súper útil cuando estamos creando sitios web!



## **`element.style.display`**

Imagina que en una página web puedes tener elementos como textos, imágenes o botones, y a veces quieres que estos elementos se vean, y otras veces no. Con **`element.style.display`** le decimos a la computadora si debe mostrar u ocultar un elemento en la página.

Es como si tuvieras un interruptor que puede encender o apagar un objeto en la página. Cuando el "interruptor" está en **"none"**, el objeto se oculta, y cuando está en **"block"**, el objeto aparece.

**¿Cómo funciona?**

1. Seleccionas un elemento usando su **ID**.

2. Usas 

   ### `element.style.display`

    para decir si quieres que ese elemento se vea o no.

   - ### Si pones `display = "none"`, el elemento desaparece.

   - ### Si pones `display = "block"`, el elemento aparece.

### Ejemplo 1: Mostrar y ocultar un párrafo

Con el primer botón ocultas el párrafo, y con el segundo lo vuelves a mostrar.

```html
<!DOCTYPE html>
<html>
<body>

<p id="miParrafo">Este es un párrafo que puedes ocultar.</p>
<button onclick="ocultar()">Ocultar</button>
<button onclick="mostrar()">Mostrar</button>

<script>
function ocultar() {
    document.getElementById("miParrafo").style.display = "none";
}

function mostrar() {
    document.getElementById("miParrafo").style.display = "block";
}
</script>

</body>
</html>
```



### Ejemplo 2: Mostrar y ocultar una imagen

Aquí puedes hacer que la imagen desaparezca y luego vuelva a aparecer usando los botones.

```html
<!DOCTYPE html>
<html>
<body>

<img id="miImagen" src="imagen.jpg" width="300">
<button onclick="esconderImagen()">Ocultar Imagen</button>
<button onclick="mostrarImagen()">Mostrar Imagen</button>

<script>
function esconderImagen() {
    document.getElementById("miImagen").style.display = "none";
}

function mostrarImagen() {
    document.getElementById("miImagen").style.display = "block";
}
</script>

</body>
</html>
```



### Ejemplo 3: Cambiar entre mostrar y ocultar una caja de texto

Este ejemplo te permite hacer que una caja azul se oculte o se muestre cada vez que haces clic en el botón.

```html
<!DOCTYPE html>
<html>
<body>

<div id="miCaja" style="width:100px; height:100px; background-color:lightblue;"></div>
<button onclick="cambiarVisibilidad()">Cambiar Visibilidad</button>

<script>
function cambiarVisibilidad() {
    var caja = document.getElementById("miCaja");
    if (caja.style.display === "none") {
        caja.style.display = "block";
    } else {
        caja.style.display = "none";
    }
}
</script>

</body>
</html>
```



**Resumen:** `element.style.display` te ayuda a decidir si un elemento debe estar visible o no en tu página web. ¡Es una herramienta muy útil para crear efectos interactivos y dinámicos!

# **Instrucciones para el Proyecto: "Astronautas en el Espacio"**

## **Objetivo:**

Crear una página web interactiva que presenta perfiles de astronautas y sus misiones, utilizando HTML, CSS, y JavaScript. Este proyecto está diseñado para que los estudiantes aprendan a estructurar una página web, aplicar estilos básicos, y agregar interactividad con JavaScript.

------

### **Paso a Paso**

#### **1. **Organización del Proyecto:

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
│   └── neil.png
│   └── yuri.png
│   └── ... (imágenes de otros astronautas)
├── js/
│   └── script.js
└── index.html
```



#### **2. Estructuración del HTML**

1. Abre `index.html` en un editor de texto (como Visual Studio Code):
   - Comienza con la estructura básica de un documento HTML.

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astronautas en el Espacio</title>
    
    <link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
      rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH"
      crossorigin="anonymous"/>
        
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Astronautas en el Espacio</h1>
    </header>
    <main>
        <!-- Contenedor de los perfiles de astronautas -->
        <section id="astronauts-container">
            <!-- Perfil de Neil Armstrong -->
            <div class="astronaut-profile">
                <h2>Neil Armstrong</h2>
                <img src="https://example.com/neil-armstrong.jpg" alt="Neil Armstrong">
                <p>Neil Armstrong fue el primer ser humano en caminar sobre la Luna durante la misión Apolo 11 en 1969.</p>
                <!-- Botón para mostrar más información -->
                <button onclick="showMoreInfo('armstrong')">Más información</button>
                <!-- Contenido adicional inicialmente oculto -->
                <div id="armstrong" class="more-info">
                    <p>Neil Armstrong nació el 5 de agosto de 1930 en Wapakoneta, Ohio. Se unió a la NASA en 1962 y voló en las misiones Gemini 8 y Apolo 11.</p>
                </div>
            </div>
            <!-- Perfil de Yuri Gagarin -->
            <div class="astronaut-profile">
                <h2>Yuri Gagarin</h2>
                <img src="https://example.com/yuri-gagarin.jpg" alt="Yuri Gagarin">
                <p>Yuri Gagarin fue el primer ser humano en viajar al espacio exterior en 1961 a bordo de la nave Vostok 1.</p>
                <!-- Botón para mostrar más información -->
                <button onclick="showMoreInfo('gagarin')">Más información</button>
                <!-- Contenido adicional inicialmente oculto -->
                <div id="gagarin" class="more-info">
                    <p>Yuri Gagarin nació el 9 de marzo de 1934 en Klushino, Rusia. Su vuelo espacial duró 108 minutos y orbitó la Tierra una vez.</p>
                </div>
            </div>
        </section>
    </main>
    <!-- Enlace al archivo JavaScript -->
    <script src="script.js"></script>
    
    <script
      src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
      integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"crossorigin="anonymous"></script>
    
    
</body>
</html>
```

1. Explicación:
   - **Header:** Contiene el título principal de la página.
   - **Main:** Sección principal que incluye contenedores para cada perfil de astronauta.
   - **JavaScript:** Los botones en cada perfil permiten mostrar más información utilizando una función JavaScript.

#### **3. Aplicación de Estilos CSS**

1. **Abre `styles.css` y agrega los siguientes estilos:**

```css
/* Estilos globales */
body {
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;
    color: #333;
    margin: 0;
    padding: 0;
}

header {
    background-color: #003366;
    color: white;
    text-align: center;
    padding: 20px 0;
}

h1 {
    margin: 0;
    font-size: 2.5em;
}

main {
    padding: 20px;
}

#astronauts-container {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
}

.astronaut-profile {
    background-color: white;
    border: 1px solid #ccc;
    border-radius: 10px;
    padding: 20px;
    width: 300px;
    text-align: center;
    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
}

.astronaut-profile img {
    width: 200px;
    border-radius: 50%;
    margin-bottom: 10px;
}

.astronaut-profile h2 {
    color: #003366;
}

.astronaut-profile p {
    font-size: 1em;
    line-height: 1.5;
}

.astronaut-profile .more-info {
    display: none;
    margin-top: 10px;
    font-size: 0.9em;
}

.astronaut-profile button {
    background-color: #0066cc;
    color: white;
    border: none;
    padding: 10px;
    cursor: pointer;
    border-radius: 5px;
    margin-top: 10px;
}

.astronaut-profile button:hover {
    background-color: #004c99;
}
```

1. Explicación:
   - **Global Styles:** Configura la fuente, colores y márgenes para el documento.
   - **Header Styles:** Estilo visual para el título de la página.
   - **Container Styles:** Utiliza flexbox para organizar los perfiles de astronautas en un diseño responsive.
   - **Profile Styles:** Diseña las tarjetas de los astronautas, aplicando bordes, sombras, y estilos para la imagen y el texto.
   - **Button Styles:** Personaliza los botones y define su comportamiento al pasar el cursor.
   - **Hidden Content:** El contenido adicional (`.more-info`) está oculto por defecto y se mostrará con JavaScript.

#### **4. Agregar Interactividad con JavaScript**

1. **Abre `script.js` y añade el siguiente código:**

```javascript
// Función para mostrar u ocultar información adicional
function showMoreInfo(id) {
    // Obtiene el elemento por su ID
    var element = document.getElementById(id);
    // Verifica el estado actual de la visualización y lo cambia
    if (element.style.display === "block") {
        element.style.display = "none";
    } else {
        element.style.display = "block";
    }
}
```

1. Explicación:
   - **Función `showMoreInfo`:** Esta función toma un `id` como parámetro y cambia la visibilidad del contenido adicional asociado con ese `id`.
   - **Interacción con HTML:** Cada botón tiene un `onclick` que llama a la función `showMoreInfo` con el `id` del contenido adicional correspondiente. La función verifica si el contenido está visible (`block`) o no, y lo alterna entre visible y oculto.

#### **5. Verificación y Pruebas**

1. **Guarda los archivos y abre `index.html` en tu navegador:**
   - Verifica que la página muestre correctamente el contenido y los estilos aplicados.
   - Asegúrate de que al hacer clic en los botones "Más información", el contenido adicional se muestre u oculte según lo esperado.
2. **Pruebas Adicionales:**
   - Añade nuevos 5 perfiles de astronautas siguiendo el mismo formato.
   - Prueba cambiar los estilos en `styles.css` para ver cómo afectan la presentación visual.