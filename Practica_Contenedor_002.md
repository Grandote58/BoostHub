# **PRACTICAS**

## **Variaciones con Contenedores y Hojas de Estilo**

Colocar una imagen, un texto y un botón dentro de un contenedor te permite realizar numerosas variaciones de estilo utilizando CSS

------

### 1. Contenedor con Imagen de Fondo y Texto Superpuesto

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Container with Background Image</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <style>
        .container-bg {
            /*background-image: url('https://via.placeholder.com/1920x1080'); /* Imagen de fondo */
            background-image: url('/img/fondo.jpg');
            background-size: cover; /* Ajustar tamaño de la imagen */
            background-position: center; /* Centrar la imagen */
            color: #fff; /* Color del texto */
            padding: 4rem; /* Espaciado interno */
            text-align: center; /* Centrar texto */
            position: relative; /* Posición relativa */
        }
        .container-bg .btn {
            background-color: rgba(0, 0, 0, 0.5); /* Botón semi-transparente */
            border: none; /* Sin borde */
        }
    </style>
</head>
<body>
    <div class="container container-bg mt-5">
        <h2>Texto Superpuesto</h2>
        <p>Este es un texto superpuesto sobre una imagen de fondo.</p>
        <a href="#" class="btn btn-primary">Click Aquí</a>
    </div>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
</body>
</html>

```

### 2. Contenedor con Imagen, Texto y Botón en Columnas

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Container with Background Image</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <style>
        .container-columns {
            padding: 2rem; /* Espaciado interno */
            border: 1px solid #dee2e6; /* Borde */
            border-radius: 0.25rem; /* Bordes redondeados */
            box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.15); /* Sombra */
        }
    </style>
</head>
<body>
    <div class="container container-columns mt-5">
        <div class="row align-items-center">
            <div class="col-md-4">
                <img src="https://via.placeholder.com/300" class="img-fluid rounded" alt="Imagen">
            </div>
            <div class="col-md-8">
                <h2>Título</h2>
                <p>Texto de descripción para acompañar la imagen.</p>
                <a href="#" class="btn btn-primary">Leer Más</a>
            </div>
        </div>
    </div>
    
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
</body>
</html>
```

### 3. Contenedor con Gradiente de Fondo y Botón Estilizado

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Container with Background Image</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <style>
        .container-gradient {
            background: linear-gradient(45deg, #2b1b19, #de4313); /* Gradiente */
            padding: 3rem; /* Espaciado interno */
            color: #fff; /* Color del texto */
            border-radius: 15px; /* Bordes redondeados */
            text-align: center; /* Centrar texto */
        }
        .container-gradient .btn {
            background-color: #fff; /* Color del botón */
            color: #de4313; /* Color del texto del botón */
            border: none; /* Sin borde */
        }
    </style>
</head>
<body>
    <div class="container container-gradient mt-5">
        <h2>Título con Gradiente</h2>
        <p>Este es un texto sobre un fondo con gradiente de color.</p>
        <a href="#" class="btn">Llamada a la Acción</a>
    </div>
    
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
</body>
</html>
```

### 4. Contenedor con Imagen de Fondo y Overlay

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Container with Background Image</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <style>
        .container-overlay {
            position: relative; /* Posición relativa */
            color: #fff; /* Color del texto */
            padding: 4rem; /* Espaciado interno */
            text-align: center; /* Centrar texto */
        }
        .container-overlay::before {
            content: ""; /* Contenido vacío para el overlay */
            position: absolute; /* Posición absoluta */
            top: 0; left: 0; right: 0; bottom: 0; /* Cubrir todo el contenedor */
            background: rgba(0, 0, 0, 0.5); /* Color del overlay */
            z-index: 1; /* Z-index para poner el overlay detrás del contenido */
        }
        .container-overlay img {
            position: absolute; /* Posición absoluta */
            top: 0; left: 0; right: 0; bottom: 0; /* Cubrir todo el contenedor */
            width: 100%; height: 100%; /* Ajustar tamaño */
            object-fit: cover; /* Ajustar la imagen */
            z-index: 0; /* Z-index para poner la imagen detrás del overlay */
        }
        .container-overlay .content {
            position: relative; /* Posición relativa */
            z-index: 2; /* Z-index para poner el contenido encima del overlay */
        }
    </style>
</head>
<body>
    <div class="container container-overlay mt-5">
        <img src="/img/fondo.jpg" alt="Background Image">
        <div class="content">
            <h2>Título con Overlay</h2>
            <p>Texto sobre una imagen de fondo con un overlay semi-transparente.</p>
            <a href="#" class="btn btn-primary">Explorar</a>
        </div>
    </div>
    
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
</body>
</html>
```

### 5. Contenedor con Efecto Hover

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Container with Background Image</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <style>
        .container-hover {
            padding: 3rem; /* Espaciado interno */
            border: 1px solid #dee2e6; /* Borde */
            border-radius: 0.25rem; /* Bordes redondeados */
            transition: transform 0.3s ease, box-shadow 0.3s ease; /* Transiciones para el efecto hover */
        }
        .container-hover:hover {
            transform: translateY(-10px); /* Desplazamiento hacia arriba */
            box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.15); /* Sombra más profunda */
        }
    </style>
</head>
<body>
    <div class="container container-hover mt-5">
        <h2>Título con Efecto Hover</h2>
        <p>Texto dentro de un contenedor con efecto hover.</p>
        <a href="#" class="btn btn-primary">Saber Más</a>
    </div>
    
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
</body>
</html>
```

# **RESUMEN**

### **Imagen de Fondo y Texto Superpuesto**:

- Utiliza `background-image`, `background-size`, y `background-position` para configurar la imagen de fondo.
- Añade estilos para el color del texto y el espaciado interno.

### **Columnas para Imagen, Texto y Botón**:

- Utiliza el sistema de grid de Bootstrap (`row`, `col-md-4`, `col-md-8`) para organizar el contenido en columnas.
- Aplica bordes, sombras y espaciado interno para un estilo de tarjeta.

### **Gradiente de Fondo**:

- Utiliza `linear-gradient` para crear un fondo con gradiente.
- Personaliza el color y estilo del botón para que contraste con el fondo.

### **Imagen de Fondo con  Overlay**:

- Utiliza `::before` pseudo-elemento para crear un overlay semi-transparente.
- Posiciona la imagen y el contenido adecuadamente utilizando `position` y `z-index`.

### **Efecto Hover**:

- Utiliza `transition` para animar transformaciones y sombras en hover.
- Añade `transform: translateY` y `box-shadow` para crear el efecto de desplazamiento y sombra.