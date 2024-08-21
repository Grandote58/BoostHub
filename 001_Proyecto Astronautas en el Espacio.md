# **Instrucciones para el Proyecto: "Astronautas en el Espacio"**

## **Objetivo:**

Crear una página web interactiva que presenta perfiles de astronautas y sus misiones, utilizando HTML, CSS, y JavaScript. Este proyecto está diseñado para que los estudiantes aprendan a estructurar una página web, aplicar estilos básicos, y agregar interactividad con JavaScript.

------

### **Paso a Paso**

#### **1. Configuración Inicial**

1. Crea la estructura del proyecto:
   - Crea una carpeta en tu computadora llamada `AstronautasEspacio`.
   - Dentro de esta carpeta, crea tres archivos: `index.html`, `styles.css`, y `script.js`.

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
   - Añade nuevos perfiles de astronautas siguiendo el mismo formato.
   - Prueba cambiar los estilos en `styles.css` para ver cómo afectan la presentación visual.