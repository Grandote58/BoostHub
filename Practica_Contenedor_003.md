# **PRACTICAS**

## **Variaciones con Contenedores de formas Geométricas**

Puedes realizar varias variaciones de un contenedor con una imagen responsiva utilizando CSS para que el contenedor adopte formas geométricas como círculo, cuadrado, rombo y hexágono.

------

### 1. Contenedor Circular

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Container with Background Image</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <style>
        .container-circle {
            width: 200px;
            height: 200px;
            border-radius: 50%; /* Hace que el contenedor sea circular */
            overflow: hidden; /* Asegura que la imagen no se salga del contenedor */
            position: relative; /* Necesario para el contenido absoluto */
        }
        .container-circle img {
            width: 100%;
            height: 100%;
            object-fit: cover; /* Asegura que la imagen cubra todo el contenedor */
        }
    </style>
</head>
<body>
    
    <div class="container mt-5">
        <div class="container-circle mx-auto">
            <img src="https://via.placeholder.com/300" alt="Circular Image">
        </div>
    </div>
    
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
</body>
</html>
```

### 2. Contenedor Cuadrado

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Container with Background Image</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <style>
        .container-square {
            width: 200px;
            height: 200px;
            overflow: hidden; /* Asegura que la imagen no se salga del contenedor */
            position: relative; /* Necesario para el contenido absoluto */
        }
        .container-square img {
            width: 100%;
            height: 100%;
            object-fit: cover; /* Asegura que la imagen cubra todo el contenedor */
        }
    </style>
</head>
<body>

    <div class="container mt-5">
        <div class="container-square mx-auto">
            <img src="https://via.placeholder.com/300" alt="Square Image">
        </div>
    </div>
    
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
</body>
</html>
```

### 3. Contenedor en Forma de Rombo

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Container with Background Image</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <style>
        .container-rhombus {
            width: 200px;
            height: 200px;
            overflow: hidden; /* Asegura que la imagen no se salga del contenedor */
            position: relative; /* Necesario para el contenido absoluto */
            transform: rotate(45deg); /* Rota el contenedor para formar un rombo */
            margin: 50px auto; /* Centra el contenedor horizontalmente */
        }
        .container-rhombus img {
            width: 100%;
            height: 100%;
            object-fit: cover; /* Asegura que la imagen cubra todo el contenedor */
            transform: rotate(-45deg); /* Rota la imagen en dirección opuesta */
        }
    </style>
</head>
<body>

    <div class="container mt-5">
        <div class="container-rhombus">
            <img src="https://via.placeholder.com/300" alt="Rhombus Image">
        </div>
    </div>
    
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
</body>
</html>
```

### 4. Contenedor Hexagonal

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Container with Background Image</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <style>
        .container-hexagon {
            width: 200px;
            height: 230px;
            background-color: #fff; /* Fondo blanco para el hexágono */
            position: relative; /* Necesario para el contenido absoluto */
            margin: 50px auto; /* Centra el contenedor horizontalmente */
            clip-path: polygon(25% 6.7%, 75% 6.7%, 100% 50%, 75% 93.3%, 25% 93.3%, 0% 50%); /* Clip-path para formar el hexágono */
            overflow: hidden; /* Asegura que la imagen no se salga del contenedor */
        }
        .container-hexagon img {
            width: 100%;
            height: 100%;
            object-fit: cover; /* Asegura que la imagen cubra todo el contenedor */
            position: absolute; /* Posición absoluta para ajustar dentro del hexágono */
            top: 0;
            left: 0;
        }
    </style>
</head>
<body>

    <div class="container mt-5">
        <div class="container-hexagon">
            <img src="https://via.placeholder.com/300" alt="Hexagonal Image">
        </div>
    </div>
    
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
</body>
</html>
```

# **RESUMEN**

### **Contenedor Circular**:

- `border-radius: 50%;`: Hace que el contenedor tenga bordes redondeados y forme un círculo.
- `overflow: hidden;`: Asegura que la imagen no se salga del contenedor.
- `img { width: 100%; height: 100%; object-fit: cover; }`: Hace que la imagen sea responsiva y cubra todo el contenedor sin distorsionarse.

### **Contenedor Cuadrado**:

- `width` y `height` fijos para definir el tamaño del contenedor.
- `overflow: hidden;`: Asegura que la imagen no se salga del contenedor.
- `img { width: 100%; height: 100%; object-fit: cover; }`: Hace que la imagen sea responsiva y cubra todo el contenedor sin distorsionarse.

### **Contenedor en Forma de Rombo**:

- `transform: rotate(45deg);`: Rota el contenedor para formar un rombo.
- `margin: 50px auto;`: Centra el contenedor horizontalmente.
- `img { transform: rotate(-45deg); }`: Rota la imagen en la dirección opuesta para corregir la orientación.

### **Contenedor Hexagonal**:

- `clip-path: polygon(...)`: Define un contorno hexagonal para el contenedor.
- `img { width: 100%; height: 100%; object-fit: cover; position: absolute; top: 0; left: 0; }`: Hace que la imagen sea responsiva, cubra todo el contenedor y se ajuste dentro del hexágono.