# ![Mesa de trabajo 1Head](http://drive.google.com/uc?export=view&id=1p2rqX0Nck3MI8LKzYct_oEMRETRIhzTH)



# Creación de un Jumbotron Personalizado con Bootstrap

### Objetivos Específicos

1. Configurar el espacio para que el contenido del jumbotron pueda ser observado en pantallas pequeñas.
2. Crear un jumbotron con un título, un texto secundario y un botón, utilizando hojas de estilo externas para personalizar sus propiedades.

### Paso a Paso

#### Paso 1: Configurar el Espacio para Pantallas Pequeñas

Para asegurarnos de que el jumbotron sea responsivo y se vea correctamente en todos los dispositivos, utilizaremos las clases de Bootstrap.

#### Paso 2: Crear la Estructura HTML del Jumbotron

#### HTML Documentado

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Jumbotron Personalizado</title>
  <!-- Incluimos el CSS de Bootstrap desde CDN -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
  <!-- Incluimos nuestra hoja de estilos personalizada -->
  <link href="styles.css" rel="stylesheet">
</head>
<body>
  <!-- Jumbotron -->
  <div class="jumbotron-custom">
    <h1 class="jumbotron-title">Bienvenidos</h1> <!-- Título del jumbotron -->
    <p class="jumbotron-subtitle">Este es un excelente proceso de aprendizaje</p> <!-- Texto secundario -->
    <a class="btn btn-custom" href="#">Leer Más</a> <!-- Botón del jumbotron -->
  </div>

  <!-- Incluimos el JS de Bootstrap desde CDN -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
</body>
</html>
```

#### CSS Documentado

```css
/* styles.css */
/* Estilo para el jumbotron */
.jumbotron-custom {
  width: 100%; /* Ancho del jumbotron */
  height: auto; /* Altura del jumbotron */
  background-color: #f8f9fa; /* Color de fondo */
  border-radius: 10px; /* Esquinas redondeadas */
  padding: 2rem 1rem; /* Relleno del jumbotron */
  text-align: center; /* Alineación del texto */
}

/* Estilo para el título del jumbotron */
.jumbotron-title {
  font-family: 'Arial', sans-serif; /* Tipo de fuente */
  font-size: 2.5rem; /* Tamaño de la fuente */
  color: #343a40; /* Color de la fuente */
  margin-bottom: 1rem; /* Margen inferior */
}

/* Estilo para el texto secundario del jumbotron */
.jumbotron-subtitle {
  font-family: 'Arial', sans-serif; /* Tipo de fuente */
  font-size: 1.5rem; /* Tamaño de la fuente */
  color: #6c757d; /* Color de la fuente */
  margin-bottom: 1.5rem; /* Margen inferior */
}

/* Estilo para el botón del jumbotron */
.btn-custom {
  background-color: #007bff; /* Color de fondo del botón */
  border-color: #007bff; /* Color del contorno del botón */
  color: #fff; /* Color del texto del botón */
  border-radius: 5px; /* Esquinas redondeadas del botón */
  padding: 0.5rem 1rem; /* Relleno del botón */
  text-transform: uppercase; /* Transformación del texto */
  text-decoration: none; /* Sin subrayado */
}

.btn-custom:hover {
  background-color: #0056b3; /* Color de fondo del botón al pasar el mouse */
  border-color: #0056b3; /* Color del contorno del botón al pasar el mouse */
}
```

# ![Mesa de trabajo 1FOOTER](http://drive.google.com/uc?export=view&id=1vwLVsNlcF2PEyv9fULe2cohQnVfwRWLg)

### Conclusión

Este tutorial proporciona los conocimientos necesarios para crear un jumbotron personalizado utilizando Bootstrap y CSS, asegurando que el contenido sea responsivo y se vea bien en cualquier dispositivo. Estas técnicas pueden aplicarse en el diseño de secciones clave de sitios web, como encabezados, promociones y llamadas a la acción.
