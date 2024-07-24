# **Contenidos WEB - Mas Profesionales**

## Diseño y Personalización de Contenedores Responsivos

### Objetivos Específicos

1. Configurar el espacio para que el contenido pueda ser observado en pantallas pequeñas.
2. Crear contenedores personalizados utilizando Bootstrap y CSS, asegurando la flexibilidad y la capacidad de modificación para diferentes elementos visuales.

### Paso a Paso

#### Paso 1: Configurar el Espacio para Pantallas Pequeñas

Utilizaremos las clases de Bootstrap para asegurarnos de que el contenido sea responsivo y se vea correctamente en todos los dispositivos.

#### Paso 2: Crear el Contenedor Principal

El contenedor principal tendrá una imagen de fondo o un color, y se asociará una hoja de estilo para su personalización.

```html
<div class="Contenedor1-p1">
  <!-- Contenido del contenedor principal -->
</div>
```

```css
.Contenedor1-p1 {
  background: url('background.jpg') no-repeat center center;
  background-size: cover;
  padding: 20px;
  color: #fff;
}
```

#### Paso 3: Crear el Contenedor Secundario Izquierdo

Este contenedor tendrá un texto principal, un título secundario y un botón personalizable.

```html
<div class="Contenedor2-p2">
  <h1>Bienvenidos</h1>
  <h3>Excelente proceso de aprendizaje para cambiar el mundo</h3>
  <button class="btn btn-custom">Más Datos</button>
</div>
```

```css
.Contenedor2-p2 {
  text-align: left;
  border: 1px solid #fff;
  border-radius: 10px;
  padding: 20px;
  background-color: rgba(0, 0, 0, 0.5);
}

.Contenedor2-p2 h1 {
  font-family: 'Arial', sans-serif;
  font-size: 2.5em;
}

.Contenedor2-p2 h3 {
  font-family: 'Arial', sans-serif;
  font-size: 1.5em;
  margin-bottom: 20px;
}

.btn-custom {
  background-color: #006400;
  border-color: #006400;
  color: #fff;
  border-radius: 10px;
  border: 1px solid #fff;
}

.btn-custom:hover {
  background-color: #004d00;
  border-color: #004d00;
}
```

#### Paso 4: Crear el Contenedor Secundario Derecho

Este contenedor tendrá una imagen con esquinas redondeadas, tamaño personalizable y transparencia.

```html
<div class="Contenedor3-p3">
  <img src="imagen.png" alt="Imagen" class="img-fluid imagen-custom">
</div>
```

```css
.Contenedor3-p3 {
  text-align: right;
}

.imagen-custom {
  width: 200px;
  height: 200px;
  border-radius: 20px;
  opacity: 0.7;
}
```

### Solución Completa

Aquí se muestra la solución completa del código HTML y CSS.

#### HTML Completo

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Contenedor Personalizado</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
  <link href="styles.css" rel="stylesheet">
</head>
<body>
  <div class="Contenedor1-p1">
    <div class="row">
      <div class="col-md-6 Contenedor2-p2">
        <h1>Bienvenidos</h1>
        <h3>Excelente proceso de aprendizaje para cambiar el mundo</h3>
        <button class="btn btn-custom">Más Datos</button>
      </div>
      <div class="col-md-6 Contenedor3-p3">
        <img src="imagen.png" alt="Imagen" class="img-fluid imagen-custom">
      </div>
    </div>
  </div>
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
</body>
</html>
```

#### CSS Completo

```css
/* styles.css */
/* Estilo para el contenedor principal */
.Contenedor1-p1 {
  background: url('background.jpg') no-repeat center center;
  background-size: cover;
  padding: 20px;
  color: #fff;
}

/* Estilo para el contenedor secundario izquierdo */
.Contenedor2-p2 {
  text-align: left;
  border: 1px solid #fff;
  border-radius: 10px;
  padding: 20px;
  background-color: rgba(0, 0, 0, 0.5);
}

.Contenedor2-p2 h1 {
  font-family: 'Arial', sans-serif;
  font-size: 2.5em;
}

.Contenedor2-p2 h3 {
  font-family: 'Arial', sans-serif;
  font-size: 1.5em;
  margin-bottom: 20px;
}

.btn-custom {
  background-color: #006400;
  border-color: #006400;
  color: #fff;
  border-radius: 10px;
  border: 1px solid #fff;
}

.btn-custom:hover {
  background-color: #004d00;
  border-color: #004d00;
}

/* Estilo para el contenedor secundario derecho */
.Contenedor3-p3 {
  text-align: right;
}

.imagen-custom {
  width: 200px;
  height: 200px;
  border-radius: 20px;
  opacity: 0.7;
}
```

### Conclusión

Este tutorial proporciona los conocimientos necesarios para crear contenedores personalizados utilizando Bootstrap y CSS, asegurando que el contenido sea responsivo y se vea bien en cualquier dispositivo. Estas técnicas pueden aplicarse en el diseño de sitios web modernos, permitiendo la personalización de secciones clave como encabezados, pies de página y bloques de contenido.





