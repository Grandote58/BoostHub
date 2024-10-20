# Práctica sencilla

Crear una página web utilizando HTML5, CSS y Bootstrap para insertar un mapa de Google Maps embebido y dos cuadros de texto donde se puedan ingresar las coordenadas (latitud y longitud), junto con un botón para "ubicar" la ubicación. 



### Objetivo:

Crear una página web sencilla que muestre un mapa embebido de Google Maps y permita a los usuarios ingresar latitud y longitud en dos cuadros de texto. Al hacer clic en el botón, la página debe mostrar las coordenadas que fueron ingresadas, simulando un cambio de ubicación.

### Instrucciones:

#### 1. **Estructura de Archivos**

La estructura del proyecto debe ser la siguiente:

```
/map_practice
    index.html
    styles.css
```

#### 2. **Código HTML5 (index.html)**

El siguiente código muestra cómo crear la página con Bootstrap, el mapa embebido, y los cuadros de texto:

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title>Mapa con Coordenadas</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="styles.css">
</head>
<body>

    <!-- Barra de navegación -->
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class="container-fluid">
            <a class="navbar-brand" href="#">Mapa Interactivo</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item">
                        <a class="nav-link active" aria-current="page" href="#">Inicio</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Mapa</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Contacto</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- Sección del mapa -->
    <div class="container mt-5">
        <div class="row">
            <div class="col-md-12 text-center">
                <h1>Ubica el Mapa</h1>
                <p class="lead">Ingresa las coordenadas para ubicar la posición</p>
            </div>
        </div>
        <div class="row justify-content-center">
            <div class="col-md-6">
                <!-- Cuadros de texto para latitud y longitud -->
                <form id="coordinatesForm">
                    <div class="mb-3">
                        <label for="latitude" class="form-label">Latitud</label>
                        <input type="text" class="form-control" id="latitude" placeholder="Ingresa la latitud">
                    </div>
                    <div class="mb-3">
                        <label for="longitude" class="form-label">Longitud</label>
                        <input type="text" class="form-control" id="longitude" placeholder="Ingresa la longitud">
                    </div>
                    <button type="button" id="locateButton" class="btn btn-primary">Ubicar</button>
                </form>
            </div>
        </div>
        
        <!-- Mapa embebido -->
        <div class="row justify-content-center mt-5">
            <div class="col-md-8">
                <iframe id="googleMap" 
                    src="https://www.google.com/maps/embed?pb=!1m14!1m12!1m3!1d3976.8546800261286!2d-74.06592242308627!3d4.71098867867047!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!5e0!3m2!1ses-419!2sco!4v1605844549996!5m2!1ses-419!2sco" 
                    width="100%" height="450" style="border:0;" allowfullscreen="" loading="lazy">
                </iframe>
            </div>
        </div>
    </div>

    <!-- Pie de página -->
    <footer class="bg-light text-center py-4 mt-5">
        <p>&copy; 2024 Mapa Interactivo. Todos los derechos reservados.</p>
    </footer>

    <script>
        // Simular la función de ubicar el mapa (sin API)
        document.getElementById('locateButton').addEventListener('click', function() {
            const latitud = document.getElementById('latitude').value;
            const longitud = document.getElementById('longitude').value;
            if (latitud && longitud) {
                alert(`Coordenadas ingresadas: Latitud: ${latitud}, Longitud: ${longitud}`);
            } else {
                alert('Por favor, ingresa ambas coordenadas.');
            }
        });
    </script>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

#### 3. **Hoja de Estilos (styles.css)**

Este archivo permite agregar algo de personalización al diseño:

```css
body {
    font-family: Arial, sans-serif;
    background-color: #f9f9f9;
    color: #333;
}

h1 {
    color: #007bff;
}

footer {
    background-color: #f8f9fa;
    padding: 10px;
}
```

### Descripción de la práctica:

- **HTML5**: Se utilizan etiquetas semánticas como `<nav>`, `<div>`, `<form>`, `<input>`, y `<iframe>`. Se agregan cuadros de texto para ingresar latitud y longitud.
- **CSS**: Se personalizan colores y fuentes en el encabezado y pie de página.
- **Bootstrap**: Se utilizan clases como `navbar`, `container`, `row`, `col-md`, `form-control`, y botones de Bootstrap para hacer la página responsive.

### Funcionamiento:

- El mapa embebido se muestra inicialmente con una ubicación predeterminada.
- El formulario permite ingresar latitud y longitud en los cuadros de texto. Aunque no se cambia realmente la ubicación en el mapa sin usar una API, al hacer clic en el botón se simula el ingreso de coordenadas mediante un `alert`.