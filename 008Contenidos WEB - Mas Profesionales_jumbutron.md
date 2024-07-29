# ![Mesa de trabajo 1Head](http://drive.google.com/uc?export=view&id=1p2rqX0Nck3MI8LKzYct_oEMRETRIhzTH)


# Creación de un Jumbotron Responsivo con Bootstrap 5

En este tutorial, aprenderás a crear un jumbotron responsivo utilizando Bootstrap 5 y HTML5. El jumbotron incluirá un título, un texto secundario, un botón y una imagen. Todos los estilos personalizados se aplicarán desde una hoja de estilo externa para mantener el código limpio y fácil de mantener.

### Paso 1: Crear la Estructura HTML

1. **Crea el archivo `index.html`** y añade el siguiente código HTML básico:

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jumbotron Responsivo</title>
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <!-- Hoja de estilos personalizada -->
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Jumbotron personalizado -->
    <div class="jumbotron custom-jumbotron d-flex align-items-center">
        <div class="container">
            <!-- Título del Jumbotron -->
            <h1 class="display-4 custom-title">Título del Jumbotron</h1>
            <!-- Texto secundario -->
            <p class="lead custom-text">Este es un texto secundario dentro del jumbotron.</p>
            <!-- Botón de acción -->
            <a class="btn btn-primary custom-button" href="#" role="button">Leer más</a>
        </div>
        <!-- Contenedor de la imagen -->
        <div class="image-container">
            <img src="https://via.placeholder.com/150" class="img-fluid rounded-circle custom-image" alt="imagen">
        </div>
    </div>

    <!-- Bootstrap JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
</body>
</html>
```

### Paso 2: Crear la Hoja de Estilos CSS

1. **Crea el archivo `styles.css`** y añade los siguientes estilos:

```css
/* styles.css */

/* Estilos para el jumbotron */
.custom-jumbotron {
    background-color: #f8f9fa; /* Color de fondo del jumbotron */
    padding: 2rem; /* Padding para el jumbotron */
    border-radius: 0.5rem; /* Esquinas redondeadas */
    height: auto; /* Altura automática */
}

/* Estilos para el título */
.custom-title {
    font-family: 'Arial', sans-serif; /* Tipo de fuente */
    color: #343a40; /* Color de la fuente */
    font-size: 2.5rem; /* Tamaño de la fuente */
    text-align: left; /* Alineación del texto */
}

/* Estilos para el texto secundario */
.custom-text {
    font-family: 'Arial', sans-serif; /* Tipo de fuente */
    color: #6c757d; /* Color de la fuente */
    font-size: 1.25rem; /* Tamaño de la fuente */
    text-align: left; /* Alineación del texto */
}

/* Estilos para el botón */
.custom-button {
    background-color: #007bff; /* Color de fondo del botón */
    border: 2px solid #007bff; /* Color del contorno */
    border-radius: 0.5rem; /* Esquinas redondeadas */
    text-align: left; /* Alineación del texto */
}

/* Estilos para la imagen */
.image-container {
    margin: 1rem 0; /* Margen superior e inferior */
    display: flex; /* Flexbox para el contenedor de la imagen */
    justify-content: center; /* Centrar horizontalmente */
}

.custom-image {
    border: 3px solid #000; /* Contorno de la imagen */
    border-radius: 50%; /* Esquinas redondeadas (círculo) */
    max-width: 150px; /* Ancho máximo */
    max-height: 150px; /* Altura máxima */
}

/* Responsividad */
@media (max-width: 768px) {
    .jumbotron {
        flex-direction: column; /* Columna en pantallas pequeñas */
        text-align: center; /* Texto centrado */
    }
  .image-container {
    margin-top: 1rem; /* Margen superior */
    margin-left: 2rem;
    margin-bottom: 1rem;
    margin-right: 5rem; /* Margen derecho */
  }
}
```

### Paso 3: Verificar la Responsividad

1. **Abre `index.html` en tu navegador** y ajusta el tamaño de la ventana para verificar que el jumbotron se visualiza correctamente en diferentes tamaños de pantalla. Asegúrate de que el diseño se adapta adecuadamente y que todos los elementos (título, texto, botón e imagen) están bien alineados y son visibles.


# ![Mesa de trabajo 1FOOTER](http://drive.google.com/uc?export=view&id=1vwLVsNlcF2PEyv9fULe2cohQnVfwRWLg)
