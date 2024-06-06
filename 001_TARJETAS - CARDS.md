# **TARJETAS - CARDS**

Las tarjetas (cards) son un componente clave en el diseño web moderno, ofreciendo una manera elegante y efectiva de organizar y presentar contenido.

Te presento la importancia y las ventajas del uso de tarjetas en el diseño web

🔹 **Organización**: Facilitan la división del contenido en secciones manejables.

🔹 **Versatilidad**: Se adaptan a diversas necesidades y contextos de uso.

🔹 **Consistencia**: Promueven un diseño coherente y uniforme.

🔹 **Interactividad**: Mejoran la participación del usuario con elementos interactivos.

🔹 **Experiencia del Usuario**: Mejoran la navegabilidad y accesibilidad del contenido.

🔹 **Adaptabilidad**: Son flexibles y se integran bien con diferentes frameworks y dispositivos.

En conclusión, el uso de tarjetas en el diseño web no solo mejora la estética de un sitio, sino que también optimiza la usabilidad y la experiencia del usuario, haciendo que la información sea más accesible, clara y atractiva.



## Plantilla de Trabajo - HTML5 & Boostrap v5.3

Recuerda cambiar los Link's y los Scripts de Boostrap cada vez que salgan nuevas actualizaciones

```html
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>

    <!-- Links de Boostrap -->
    
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css">

    <!-- Hojas de Estilo -->


</head>
<body>



    <!-- Scripts de Boostrap -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
   
</body>
</html>
```



# **Practicas**

## 1. Card con Fondo Gradiente

```css
    <!-- Hojas de Estilo -->
    <style>

    .card-custom-gradient {
        background: linear-gradient(135deg, #ff6f61, #de4313);
        color: #fff;
    }
    .card-custom-gradient .card-footer {
        background-color: rgba(0, 0, 0, 0.1);
    }

    </style>
```

```html
    <div class="card card-custom card-custom-gradient">
        <div class="card-body text-center">
            <i class="bi bi-star card-icon"></i>
            <h5 class="card-title mt-3">Gradient Card</h5>
            <p class="card-text">This card has a gradient background and customized footer.</p>
            <a href="#" class="btn btn-custom">Learn More</a>
        </div>

        
        <div class="card-footer text-center">
            <small>Footer Content</small>
        </div>
    </div>  
```

## 2. Card con Borde Redondeado y Sombra

```css
    <!-- Hojas de Estilo -->
    <style>

    .card-custom-rounded {
        border-radius: 1rem;
        box-shadow: 0 1rem 3rem rgba(0, 0, 0, 0.175);
    }

    </style>
```

```html
    <div class="card card-custom card-custom-rounded">
        <div class="card-body text-center">
            <i class="bi bi-heart card-icon"></i>
            <h5 class="card-title mt-3">Rounded Card</h5>
            <p class="card-text">This card has rounded corners and a larger shadow effect.</p>
            <a href="#" class="btn btn-custom">Learn More</a>
        </div>
        <div class="card-footer text-center">
            <small>Footer Content</small>
        </div>
    </div>
```

## 3. Card con Animación de Entrada

```css
    <!-- Hojas de Estilo -->
    <style>
        .card-custom-animated {
            animation: fadeInUp 1s ease-in-out;
        }
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
    </style>
```

```html
    <div class="card card-custom card-custom-animated">
        <div class="card-body text-center">
            <i class="bi bi-rocket card-icon"></i>
            <h5 class="card-title mt-3">Animated Card</h5>
            <p class="card-text">This card has a fade-in-up animation effect when it loads.</p>
            <a href="#" class="btn btn-custom">Learn More</a>
        </div>
        <div class="card-footer text-center">
            <small>Footer Content</small>
        </div>
    </div>
```

## 4. Card con Icono en el Fondo

```css
    <!-- Hojas de Estilo -->
    <style>
        .card-custom-background-icon {
            position: relative;
            overflow: hidden;
        }
        .card-custom-background-icon::before {
            content: "\F3C9"; /* Unicode for star icon */
            font-family: 'Bootstrap Icons';
            font-size: 8rem;
            color: rgba(0, 0, 0, 0.1);
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 0;
        }
        .card-custom-background-icon .card-body {
            position: relative;
            z-index: 1;
        }
    </style>
```

```html
    <div class="card card-custom card-custom-background-icon">
        <div class="card-body text-center">
            <i class="bi bi-fingerprint"></i>
            <h5 class="card-title mt-3">Background Icon Card</h5>
            <p class="card-text">This card has a large, semi-transparent icon in the background.</p>
            <a href="#" class="btn btn-custom">Learn More</a>
        </div>
        <div class="card-footer text-center">
            <small>Footer Content</small>
        </div>
    </div>
```

## 5. Card con Efecto Hover en el Botón

```css
    <!-- Hojas de Estilo -->
    <style>
        .btn-hover-custom {
            background-color: #28a745;
            color: #fff;
            border: none;
            transition: background-color 0.3s ease, transform 0.3s ease;
        }
        .btn-hover-custom:hover {
            background-color: #218838;
            transform: scale(1.05);
        }
    </style>
```

```html
    <div class="card card-custom">
        <div class="card-body text-center">
            <i class="bi bi-emoji-smile card-icon"></i>
            <h5 class="card-title mt-3">Hover Effect Button</h5>
            <p class="card-text">This card has a button with a hover effect that changes color and scales up.</p>
            <a href="#" class="btn btn-hover-custom">Learn More</a>
        </div>
        <div class="card-footer text-center">
            <small>Footer Content</small>
        </div>
    </div>
```



## 6. Card Básico Personalizado, aplicando todos los argumentos anteriores

```css
    <!-- Hojas de Estilo -->
    <style>
        .card-custom {
            width: 18rem; /* Ancho personalizado */
            border: 1px solid #dee2e6;
            border-radius: 0.25rem;
            box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.15);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .card-custom:hover {
            transform: translateY(-10px);
            box-shadow: 0 1rem 2rem rgba(0, 0, 0, 0.25);
        }
        .card-icon {
            font-size: 3rem;
            color: #007bff;
        }
        .card-title {
            font-size: 1.5rem;
            font-weight: bold;
        }
        .card-text {
            font-size: 1rem;
            color: #6c757d;
        }
        .card-footer {
            background-color: #f8f9fa;
            border-top: 1px solid #dee2e6;
        }
        .btn-custom {
            background-color: #007bff;
            color: #fff;
            border: none;
            transition: background-color 0.3s ease;
        }
        .btn-custom:hover {
            background-color: #0056b3;
        }
    </style>
```

```html
    <div class="container mt-5">
        <div class="card card-custom">
            <div class="card-body text-center">
                <i class="bi bi-star card-icon"></i>
                <h5 class="card-title mt-3">Custom Card</h5>
                <p class="card-text">This is an example of a custom card with a Bootstrap icon, text, and a button.</p>
                <a href="#" class="btn btn-custom">Learn More</a>
            </div>
            <div class="card-footer text-center">
                <small>Footer Content</small>
            </div>
        </div>
    </div>
```

# **Explicación General**

1. **Iconos de Bootstrap**:
   - `<i class="bi bi-star"></i>`: Utiliza la clase de Bootstrap Icons para agregar iconos.
2. **Variaciones de CSS**:
   - **Gradientes**: Utiliza `background: linear-gradient(...)` para aplicar gradientes.
   - **Bordes Redondeados y Sombras**: Usa `border-radius` y `box-shadow` para ajustar bordes y sombras.
   - **Animaciones**: Define animaciones con `@keyframes` y aplica con `animation`.
   - **Iconos en el Fondo**: Utiliza `::before` para agregar iconos grandes y semi-transparentes en el fondo del card.
   - **Efectos Hover**: Cambia estilos como `background-color` y `transform` en el estado `:hover`.
3. **Transiciones**:
   - Utiliza `transition` para animar cambios de estilo de forma suave.











