

## **Trabajando con Bootstrap - Desarrollo Rápido**

## **Practica 001**

Ejemplo de un menú centrado en una página estilo Landín Page utilizando Bootstrap 5.0. La estructura HTML5 incluye un `nav` para el menú, un `header` para la imagen principal con texto y botón, y un `section` para contenido adicional.

1. Plantilla de HTML5

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```

2. Agrego CDN de la pagina de [Bootstrap](https://getbootstrap.com/)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>

    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">

</head>
<body>
    
    <!-- Script-->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
</body>
</html>
```

3. Agrego una barra de navegación, `nav` para el menú; después del `body` coloco la siguiente codificación

   ```html
     <!-- Navbar -->
   <nav class="navbar navbar-expand-lg navbar-custom">
       <div class="container">
           <a class="navbar-brand" href="#">
               <img src="https://cdn2.vectorstock.com/i/1000x1000/00/31/menu-restaurant-cover-icon-vector-10440031.jpg" alt="" width="30" height="30">
               Grandote58
           </a>
           <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
   
               <span class="navbar-toggler-icon"></span>
           </button>
           <div class="collapse navbar-collapse justify-content-center" id="navbarNav">
               <ul class="navbar-nav">
                   <li class="nav-item">
                       <a class="nav-link active" aria-current="page" href="#">Home</a>
                   </li>
                   <li class="nav-item">
                       <a class="nav-link" href="#">About</a>
                   </li>
                   <li class="nav-item">
                       <a class="nav-link" href="#">Services</a>
                   </li>
                   <li class="nav-item">
                       <a class="nav-link" href="#">Contact</a>
                   </li>
               </ul>
           </div>
       </div>
   </nav>
   ```

   4. Agrego secciones adicionales para agregar contenido

```html
    <!-- Header with Image and Text -->
    <header class="header-content">
        <div class="container">
            <h1>Welcome to Our Landing Page</h1>
            <p>Your success starts here</p>
            <a href="#" class="btn btn-primary btn-lg">Get Started</a>
        </div>
    </header>

    <!-- Additional Content Section -->
    <section class="py-5">
        <div class="container text-center">
            <h2>Our Services</h2>
            <p>Explore the range of services we offer to help you achieve your goals.</p>
            <!-- Add more content as needed -->
        </div>
    </section>    
```

5. Mejoremos la apariencia, utilizando un recurso de hojas de estilo

   ```css
       <style>
   
           .navbar-custom {
               background-color: #f10101;
           }
           .navbar-custom .navbar-brand,
           .navbar-custom .nav-link {
               color: #ffffff;
           }
           .header-content {
               height: 100vh;
               background: url('https://s1.1zoom.me/b5563/490/Hamburger_Closeup_Fast_food_Hands_557995_1920x1080.jpg') no-repeat center center;
   
               
               background-size: cover;
               display: flex;
               align-items: center;
               justify-content: center;
               color: #cedee9;
               text-align: center;
           }
           .header-content h1 {
               font-size: 4rem;
           }
           .header-content p {
               font-size: 1.5rem;
           }
       </style>
   ```

   

## Explicación del código:

1. **Estructura HTML5**:
   - `<nav>`: Contiene el menú de navegación.
   - `<header>`: Contiene la imagen principal, el texto y el botón.
   - `<section>`: Sección adicional para más contenido.
2. **Clases de Bootstrap**:
   - `navbar navbar-expand-lg navbar-custom`: Define la barra de navegación personalizada.
   - `navbar-toggler`, `navbar-toggler-icon`, `collapse navbar-collapse`, `navbar-nav`, `nav-item`, `nav-link`: Clases de Bootstrap para el menú de navegación.
   - `header-content`: Estilo personalizado para centrar el contenido del encabezado.
3. **CSS Personalizado**:
   - `.navbar-custom`: Define un color de fondo personalizado para el navbar.
   - `.header-content`: Define la altura, la imagen de fondo y centra el contenido del encabezado.
4. **Botón**:
   - `btn btn-primary btn-lg`: Clases de Bootstrap para estilizar el botón.





