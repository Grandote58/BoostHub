# **PRACTICAS**

## **Variaciones con Contenedores y Hojas de Estilo**

Utilizando hojas de estilo CSS para personalizar un contenedor en Bootstrap 5.0.

------

### 1.  Contenedor con Fondo Personalizado

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Custom Container</title>
    <link href="https://stackpath.bootstrapcdn.com/bootstrap/5.0.0/css/bootstrap.min.css" rel="stylesheet">
    <style>
        .caja-personalizada {
            background-color: #aac9e7; /* Color de fondo personalizado */
            padding: 2rem; /* Espaciado interno */
            border-radius: 10px; /* Bordes redondeados */
        }
    </style>
</head>
<body>
    <div class="container caja-personalizada mt-5">
        <h2>Contenedor con Fondo Personalizado</h2>
        <p>Este contenedor tiene un color de fondo personalizado, espaciado interno y bordes redondeados.</p>
    </div>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/5.0.0/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

### 2. Contenedor con Sombra y Bordes

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Custom Container</title>
    <link href="https://stackpath.bootstrapcdn.com/bootstrap/5.0.0/css/bootstrap.min.css" rel="stylesheet">
    <style>
        .caja-personalizada-borde {
            border: 2px solid #579add; /* Borde personalizado */
            padding: 2rem; /* Espaciado interno */
            box-shadow: 0 4px 8px rgba(219, 11, 11, 0.5); /* Sombra */
        }
    </style>
</head>
<body>
    <div class="container caja-personalizada-borde mt-5">
        <h2>Contenedor con Sombra y Bordes</h2>
        <p>Este contenedor tiene un borde y sombra personalizados, además de espaciado interno.</p>
    </div>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/5.0.0/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

### 3. Contenedor con Imagen de Fondo

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Custom Container</title>
    <link href="https://stackpath.bootstrapcdn.com/bootstrap/5.0.0/css/bootstrap.min.css" rel="stylesheet">
    <style>
        .caja-personalizada-img {
            /*background-image: url('https://via.placeholder.com/1920x1080'); /* Imagen de fondo */
            background-image: url('/img/fondo.jpg');
            background-size: cover; /* Ajustar tamaño de la imagen */
            background-position: center; /* Centrar la imagen */
            color: #e2d4d4; /* Color de texto */
            padding: 4rem; /* Espaciado interno */
            border-radius: 10px; /* Bordes redondeados */
        }
    </style>
</head>
<body>
    <div class="container caja-personalizada-img mt-5">
        <h2>Contenedor con Imagen de Fondo</h2>
        <p>Este contenedor tiene una imagen de fondo, color de texto blanco y bordes redondeados.</p>
    </div>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/5.0.0/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

### 4. Contenedor con Gradiente de Fondo

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Custom Container</title>
    <link href="https://stackpath.bootstrapcdn.com/bootstrap/5.0.0/css/bootstrap.min.css" rel="stylesheet">
    <style>
        .caja-personalizada-gradient {
            background: linear-gradient(45deg, #e02b1a, #290a9c); /* Gradiente */
            padding: 3rem; /* Espaciado interno */
            color: #fff; /* Color de texto */
            border-radius: 15px; /* Bordes redondeados */
        }
    </style>
</head>
<body>
    <div class="container caja-personalizada-gradient mt-5">
        <h2>Contenedor con Gradiente de Fondo</h2>
        <p>Este contenedor tiene un fondo de gradiente y un color de texto blanco.</p>
    </div>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/5.0.0/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

### 5. Contenedor con Estilo de Tarjeta

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Custom Container</title>
    <link href="https://stackpath.bootstrapcdn.com/bootstrap/5.0.0/css/bootstrap.min.css" rel="stylesheet">
    <style>
        .caja-personalizada-card {
            padding: 2rem; /* Espaciado interno */
            border: 1px solid #d6e8fa; /* Borde */
            border-radius: 0.25rem; /* Bordes redondeados */
            box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.15); /* Sombra */
            background-color: #f12f2f; /* Color de fondo */
        }
    </style>
</head>
<body>
    <div class="container caja-personalizada-card mt-5">
        <h2>Contenedor con Estilo de Tarjeta</h2>
        <p>Este contenedor tiene un estilo similar a una tarjeta, con borde, sombra y fondo blanco.</p>
    </div>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/5.0.0/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

# **RESUMEN**

### **Clases Personalizadas**:

- Cada contenedor tiene una clase CSS personalizada (`caja-personalizada`, `caja-personalizada-card`, etc.) para aplicar estilos únicos.

### **Estilos CSS**:

- **background-color**: Define el color de fondo del contenedor.
- **padding**: Añade espaciado interno para separar el contenido de los bordes.
- **border-radius**: Aplica bordes redondeados.
- **box-shadow**: Añade sombra al contenedor para darle un efecto de profundidad.
- **background-image**: Establece una imagen de fondo.
- **background-size**: Ajusta el tamaño de la imagen de fondo para cubrir todo el contenedor.
- **background-position**: Centra la imagen de fondo.
- **background**: Define un gradiente como fondo.

### Variaciones:

- **Color de Fondo**: Puedes cambiar `background-color` a cualquier color que desees.
- **Bordes**: Ajusta `border` y `border-radius` para cambiar el estilo de los bordes.
- **Sombras**: Modifica `box-shadow` para cambiar el efecto de sombra.
- **Imagen de Fondo**: Cambia la URL en `background-image` para usar diferentes imágenes.
- **Gradientes**: Experimenta con diferentes combinaciones de colores y ángulos en `linear-gradient`.
- **Texto**: Cambia `color` para ajustar el color del texto según el fondo.