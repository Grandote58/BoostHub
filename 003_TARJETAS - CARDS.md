# **Tarjetas Personalizadas con Imágenes** 

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



## Ejemplo 1: Tarjeta con Sombra y Bordes Redondeados

```css
    <style>
        .card-custom {
            border-radius: 15px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s;
        }
        .card-custom:hover {
            transform: translateY(-10px);
        }
        .card-img-top {
            border-radius: 15px 15px 0 0;
        }
    </style>
```

```html
    <div class="container mt-5">
        <div class="row">
            <div class="col-md-4 mb-4">
                <div class="card card-custom">
                    <img src="https://via.placeholder.com/300" class="card-img-top" alt="Image 1">
                    <div class="card-body">
                        <h5 class="card-title">Card with Rounded Borders</h5>
                        <p class="card-text">This card has rounded borders and a shadow effect.</p>
                        <a href="#" class="btn btn-primary">Learn More</a>
                    </div>
                </div>
            </div>
        </div>
    </div>
```

## Ejemplo 2: Tarjeta con Gradiente de Fondo

```css
    <style>
        .card-custom-gradient {
            background: linear-gradient(135deg, #ff6f61, #de4313);
            color: white;
            border-radius: 15px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s;
        }
        .card-custom-gradient:hover {
            transform: translateY(-10px);
        }
        .card-img-top {
            border-radius: 15px 15px 0 0;
        }
    </style>
```

```html
    <div class="container mt-5">
        <div class="row">
            <div class="col-md-4 mb-4">
                <div class="card card-custom-gradient">
                    <img src="https://via.placeholder.com/300" class="card-img-top" alt="Image 2">
                    <div class="card-body">
                        <h5 class="card-title">Card with Gradient Background</h5>
                        <p class="card-text">This card has a gradient background and a shadow effect.</p>
                        <a href="#" class="btn btn-light">Learn More</a>
                    </div>
                </div>
            </div>
        </div>
    </div>
```

## Ejemplo 3: Tarjeta con Animación de Entrada

```css
    <style>
        .card-custom-animated {
            border-radius: 15px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
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
        .card-img-top {
            border-radius: 15px 15px 0 0;
        }
    </style>
```

```html
    <div class="container mt-5">
        <div class="row">
            <div class="col-md-4 mb-4">
                <div class="card card-custom-animated">
                    <img src="https://via.placeholder.com/300" class="card-img-top" alt="Image 3">
                    <div class="card-body">
                        <h5 class="card-title">Card with Entry Animation</h5>
                        <p class="card-text">This card has a fade-in-up animation effect.</p>
                        <a href="#" class="btn btn-primary">Learn More</a>
                    </div>
                </div>
            </div>
        </div>
    </div>
```

## Ejemplo 4: Tarjeta con Icono en el Fondo

```css
    <style>
        .card-custom-background-icon {
            position: relative;
            overflow: hidden;
            border-radius: 15px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s;
        }
        .card-custom-background-icon::before {
            content: "\f005"; /* Unicode for star icon */
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
        .card-custom-background-icon:hover {
            transform: translateY(-10px);
        }
        .card-img-top {
            border-radius: 15px 15px 0 0;
        }
    </style>
```

```html
    <div class="container mt-5">
        <div class="row">
            <div class="col-md-4 mb-4">
                <div class="card card-custom-background-icon">
                    <img src="https://via.placeholder.com/300" class="card-img-top" alt="Image 4">
                    <div class="card-body">
                        <h5 class="card-title">Card with Background Icon</h5>
                        <p class="card-text">This card has a large, semi-transparent icon in the background.</p>
                        <a href="#" class="btn btn-primary">Learn More</a>
                    </div>
                </div>
            </div>
        </div>
    </div>
```

## Ejemplo 5: Tarjeta con Efecto Hover en el Botón

```css
    <style>
        .card-custom-hover {
            border-radius: 15px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s;
        }
        .card-custom-hover:hover {
            transform: translateY(-10px);
        }
        .card-img-top {
            border-radius: 15px 15px 0 0;
        }
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
    <div class="container mt-5">
        <div class="row">
            <div class="col-md-4 mb-4">
                <div class="card card-custom-hover">
                    <img src="https://via.placeholder.com/300" class="card-img-top" alt="Image 5">
                    <div class="card-body">
                        <h5 class="card-title">Card with Hover Effect</h5>
                        <p class="card-text">This card has a button with a hover effect that changes color and scales up.</p>
                        <a href="#" class="btn btn-hover-custom">Learn More</a>
                    </div>
                </div>
            </div>
        </div>
    </div>
```



# **Explicación General**

1. **Tarjeta con Sombra y Bordes Redondeados**:
   - `border-radius: 15px`: Redondea las esquinas de la tarjeta.
   - `box-shadow`: Añade una sombra alrededor de la tarjeta.
   - `transition: transform 0.3s`: Añade una transición suave al transformar la tarjeta en hover.
2. **Tarjeta con Gradiente de Fondo**:
   - `background: linear-gradient(...)`: Aplica un fondo de gradiente a la tarjeta.
   - `color: white`: Cambia el color del texto para que sea visible sobre el gradiente.
3. **Tarjeta con Animación de Entrada**:
   - `animation: fadeInUp 1s ease-in-out`: Aplica una animación de entrada a la tarjeta.
   - `@keyframes fadeInUp`: Define la animación de entrada.
4. **Tarjeta con Icono en el Fondo**:
   - `::before`: Utiliza el pseudo-elemento `::before` para añadir un icono de fondo.
   - `position: relative`: Asegura que el contenido de la tarjeta esté por encima del icono de fondo.
5. **Tarjeta con Efecto Hover en el Botón**:
   - `background-color`: Define el color del botón.
   - `transition`: Añade una transición suave al cambiar el color y el tamaño del botón en hover.
   - `transform: scale(1.05)`: Escala el botón cuando el usuario pasa el cursor sobre él.









