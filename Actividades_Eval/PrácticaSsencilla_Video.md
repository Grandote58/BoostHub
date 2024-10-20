# Práctica sencilla 

Crear una página web utilizando HTML5, CSS y Bootstrap para agregar un video embebido:

### Objetivo:

Crear una página web sencilla que muestre un video embebido, con un diseño responsive utilizando Bootstrap.

### Instrucciones:

#### 1. **Estructura de Archivos**

La estructura del proyecto debe ser la siguiente:

```css
/video_practice
    index.html
    styles.css
    /videos
        nature.mp4
```

#### 2. **Código HTML5 (index.html)**

El siguiente código muestra cómo crear la página con Bootstrap y un video embebido:

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title>Video Embebido - Nature</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="styles.css">
</head>
<body>

    <!-- Barra de navegación -->
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class="container-fluid">
            <a class="navbar-brand" href="#">Nature Videos</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item">
                        <a class="nav-link active" aria-current="page" href="#">Inicio</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Videos</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Contacto</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- Sección principal -->
    <div class="container mt-5">
        <div class="row">
            <div class="col-md-12 text-center">
                <h1>Explora la Belleza de la Naturaleza</h1>
                <p class="lead">Disfruta de este maravilloso video sobre paisajes naturales</p>
            </div>
        </div>
        <div class="row justify-content-center">
            <div class="col-md-8">
                <!-- Video embebido -->
                <video controls class="embed-responsive embed-responsive-16by9 w-100">
                    <source src="videos/nature.mp4" type="video/mp4">
                    Tu navegador no soporta la etiqueta de video.
                </video>
            </div>
        </div>
    </div>

    <!-- Pie de página -->
    <footer class="bg-light text-center py-4">
        <p>&copy; 2024 Nature Videos. Todos los derechos reservados.</p>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

#### 3. **Hoja de Estilos (styles.css)**

Este archivo permitirá agregar un poco de personalización al diseño:

```css
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    color: #333;
}

h1 {
    color: #4CAF50;
}

footer {
    background-color: #f8f9fa;
    padding: 10px;
}

video {
    border: 3px solid #4CAF50;
    border-radius: 8px;
}
```

#### 4. **Descripción de la práctica**

- **HTML5**: Se utilizaron etiquetas semánticas como `<nav>`, `<div>`, `<h1>`, y `<video>`. Se agregaron enlaces en la barra de navegación con Bootstrap.
- **CSS**: Se personalizó el color del texto, el estilo del borde del video y la apariencia del pie de página.
- **Bootstrap**: Se usaron clases como `navbar`, `container`, `row`, `col-md`, `lead`, y `embed-responsive` para hacer que el diseño sea responsive y compatible con dispositivos móviles.