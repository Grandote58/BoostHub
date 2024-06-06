# **Layout de Grid con Tarjetas Personalizadas**

El uso de layouts de Grid en el diseño web es crucial por varias razones, ya que proporcionan una estructura sólida y flexible para organizar contenido de manera efectiva y atractiva.

### 1. **Organización y Estructuración del Contenido**

- **Claridad Visual**: Los layouts de Grid permiten organizar el contenido en filas y columnas, lo que mejora la claridad visual y facilita la lectura.
- **Consistencia**: Proporcionan una estructura consistente en todo el sitio web, lo que ayuda a los usuarios a entender rápidamente la disposición del contenido.

### 2. **Responsividad**

- **Diseño Adaptable**: Los grids permiten crear diseños que se adaptan a diferentes tamaños de pantalla y dispositivos, desde móviles hasta desktops, garantizando una experiencia de usuario óptima.
- **Flexibilidad**: Los sistemas de Grid, como el de Bootstrap, permiten ajustar el diseño de manera fácil y flexible mediante clases predefinidas.

### 3. **Facilidad de Implementación**

- **Componentes Reutilizables**: Los layouts de Grid facilitan la reutilización de componentes, lo que reduce el tiempo de desarrollo y mantenimiento.
- **Simplicidad**: Proveen un marco sencillo para implementar diseños complejos sin necesidad de escribir mucho CSS personalizado.

### 4. **Estética y Diseño**

- **Diseño Moderno**: Los grids permiten crear diseños modernos y atractivos que son visualmente agradables.
- **Proporción y Balance**: Ayudan a mantener las proporciones y el balance en el diseño, creando una experiencia visual armoniosa.

### 5. **Mejora de la Experiencia del Usuario (UX)**

- **Navegación Intuitiva**: La organización clara y consistente facilita la navegación y mejora la usabilidad del sitio.
- **Accesibilidad**: Contribuyen a hacer el contenido más accesible al permitir un diseño claro y lógico.

### 6. **Compatibilidad con Frameworks y Herramientas**

- **Integración con Frameworks**: Los layouts de Grid son compatibles con la mayoría de los frameworks de CSS y JavaScript, como Bootstrap, Foundation y CSS Grid, lo que facilita su implementación.
- **Herramientas de Diseño**: Son compatibles con diversas herramientas de diseño y desarrollo, lo que agiliza el proceso de creación y modificación de layouts.

## **Plantilla de Trabajo**

Recuerda cambiar los Link's y los Scripts de Boostrap cada vez que salgan nuevas actualizaciones

```html
<!DOCTYPE html>
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

## 1. Tarjetas con Fondo Gradiente

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
    <div class="col-md-4 mb-4">
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
    </div>
```

## 2. Tarjetas con Borde Redondeado y Sombra

```css
    <style>
        .card-custom-rounded {
            border-radius: 1rem;
            box-shadow: 0 1rem 3rem rgba(0, 0, 0, 0.175);
        }
    </style>
```

```html
    <div class="col-md-4 mb-4">
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
    </div>
```

## 3. **Tarjetas con Animación de Entrada**

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
    <div class="col-md-4 mb-4">
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
    </div>
```

## 4. **Grid con Tarjetas Personalizadas** Completo 01

```css
 <!-- Hojas de Estilo -->
    <style>
        .card-custom {
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
        <div class="row">
            <div class="col-md-4 mb-4">
                <div class="card card-custom">
                    <div class="card-body text-center">
                        <i class="bi bi-star card-icon"></i>
                        <h5 class="card-title mt-3">Custom Card 1</h5>
                        <p class="card-text">This is an example of a custom card with a Bootstrap icon, text, and a button.</p>
                        <a href="#" class="btn btn-custom">Learn More</a>
                    </div>
                    <div class="card-footer text-center">
                        <small>Footer Content</small>
                    </div>
                </div>
            </div>
            <div class="col-md-4 mb-4">
                <div class="card card-custom">
                    <div class="card-body text-center">
                        <i class="bi bi-heart card-icon"></i>
                        <h5 class="card-title mt-3">Custom Card 2</h5>
                        <p class="card-text">This is another example of a custom card with a different icon and text.</p>
                        <a href="#" class="btn btn-custom">Learn More</a>
                    </div>
                    <div class="card-footer text-center">
                        <small>Footer Content</small>
                    </div>
                </div>
            </div>
            <div class="col-md-4 mb-4">
                <div class="card card-custom">
                    <div class="card-body text-center">
                        <i class="bi bi-rocket card-icon"></i>
                        <h5 class="card-title mt-3">Custom Card 3</h5>
                        <p class="card-text">This is yet another example of a custom card with a unique icon and text.</p>
                        <a href="#" class="btn btn-custom">Learn More</a>
                    </div>
                    <div class="card-footer text-center">
                        <small>Footer Content</small>
                    </div>
                </div>
            </div>
        </div>
    </div>
```

## 6. **Grid con Tarjetas Personalizadas** Completo 02

```css
    <!-- Hojas de Estilo -->
    <style>
        
        .card-custom {
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
        /* Variaciones */
        .card-custom-gradient {
            background: linear-gradient(135deg, #ff6f61, #de4313);
            color: #fff;
        }
        .card-custom-gradient .card-footer {
            background-color: rgba(0, 0, 0, 0.1);
        }
        .card-custom-rounded {
            border-radius: 1rem;
            box-shadow: 0 1rem 3rem rgba(0, 0, 0, 0.175);
        }
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
        .card-custom-background-icon {
            position: relative;
            overflow: hidden;
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
            <!-- Tarjeta con estilo base -->
            <div class="col-md-4 mb-4">
                <div class="card card-custom">
                    <div class="card-body text-center">
                        <i class="bi bi-star card-icon"></i>
                        <h5 class="card-title mt-3">Custom Card 1</h5>
                        <p class="card-text">This is an example of a custom card with a Bootstrap icon, text, and a button.</p>
                        <a href="#" class="btn btn-custom">Learn More</a>
                    </div>
                    <div class="card-footer text-center">
                        <small>Footer Content</small>
                    </div>
                </div>
            </div>
            <!-- Tarjeta con fondo gradiente -->
            <div class="col-md-4 mb-4">
                <div class="card card-custom card-custom-gradient">
                    <div class="card-body text-center">
                        <i class="bi bi-heart card-icon"></i>
                        <h5 class="card-title mt-3">Gradient Card</h5>
                        <p class="card-text">This card has a gradient background and customized footer.</p>
                        <a href="#" class="btn btn-custom">Learn More</a>
                    </div>
                    <div class="card-footer text-center">
                        <small>Footer Content</small>
                    </div>
                </div>
            </div>
            <!-- Tarjeta con borde redondeado y sombra -->
            <div class="col-md-4 mb-4">
                <div class="card card-custom card-custom-rounded">
                    <div class="card-body text-center">
                        <i class="bi bi-rocket card-icon"></i>
                        <h5 class="card-title mt-3">Rounded Card</h5>
                        <p class="card-text">This card has rounded corners and a larger shadow effect.</p>
                        <a href="#" class="btn btn-custom">Learn More</a>
                    </div>
                    <div class="card-footer text-center">
                        <small>Footer Content</small>
                    </div>
                </div>
            </div>
            <!-- Tarjeta con animación de entrada -->
            <div class="col-md-4 mb-4">
                <div class="card card-custom card-custom-animated">
                    <div class="card-body text-center">
                        <i class="bi bi-lightning-fill card-icon"></i>
                        <h5 class="card-title mt-3">Animated Card</h5>
                        <p class="card-text">This card has a fade-in-up animation effect when it loads.</p>
                        <a href="#" class="btn btn-custom">Learn More</a>
                    </div>
                    <div class="card-footer text-center">
                        <small>Footer Content</small>
                    </div>
                </div>
            </div>
            <!-- Tarjeta con icono en el fondo -->
            <div class="col-md-4 mb-4">
                <div class="card card-custom card-custom-background-icon">
                    <div class="card-body text-center">
                        <i class="bi bi-star card-icon"></i>
                        <h5 class="card-title mt-3">Background Icon Card</h5>
                        <p class="card-text">This card has a large, semi-transparent icon in the background.</p>
                        <a href="#" class="btn btn-custom">Learn More</a>
                    </div>
                    <div class="card-footer text-center">
                        <small>Footer Content</small>
                    </div>
                </div>
            </div>
            <!-- Tarjeta con efecto hover en el botón -->
            <div class="col-md-4 mb-4">
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
            </div>
        </div>
    </div>
```

# **Explicación de las Variaciones**

1. **Tarjeta con Fondo Gradiente**:
   - Utiliza `background: linear-gradient(...)` para aplicar un fondo gradiente.
   - Cambia el color del texto y el fondo del pie de la tarjeta.
2. **Tarjeta con Borde Redondeado y Sombra**:
   - Utiliza `border-radius` para redondear las esquinas de la tarjeta.
   - Aplica una sombra más pronunciada con `box-shadow`.
3. **Tarjeta con Animación de Entrada**:
   - Define una animación con `@keyframes` y aplica con `animation`.
   - Anima la opacidad y la posición de la tarjeta cuando carga.
4. **Tarjeta con Icono en el Fondo**:
   - Usa `::before` para añadir un icono grande y semi-transparente en el fondo de la tarjeta.
   - Asegura que el contenido de la tarjeta esté en un nivel superior con `z-index`.
5. **Tarjeta con Efecto Hover en el Botón**:
   - Utiliza `:hover` para cambiar el color y el tamaño del botón cuando el usuario pasa el cursor sobre él.
   - Aplica una transición suave con `transition`.







