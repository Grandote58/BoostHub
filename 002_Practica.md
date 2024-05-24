# **Practica Tarjetas**

La siguiente practica crea tres tarjetas con contenido mixto (imágenes, texto y un botón) dentro de un contenedor. El diseño será responsivo y utiliza clases de Bootstrap para asegurar que se vea bien en diferentes tamaños de pantalla.

1. Estructura inicial de una pagina HTML5 y responsiva.

   Recuerda que debes agregar los enlaces CDN de la pagina de [Bootstrap](https://getbootstrap.com/)

   

   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
   
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>Responsive Cards</title>
   
       <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
   
   </head>
   
   <body>
   
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
               </ul>
           </div>
       </div>
   </nav>
   
       <!-- Aqui colocaras las tarjetas responsivas -->
       
   <!-- Script -->
   <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
   
   </body>
   </html>
   ```

2. Antes de agregar las tarjetas, es necesario estructurar el espacio donde se colocarán utilizando un contenedor. 

   ```html
   <!-- Contenedor principal -->
   <div class="container mt-5">
       <!-- Fila para contener las tarjetas -->
       <div class="row justify-content-center">
       
        <!-- Aqui codigo de las tarjetas -->
           
       </div>
   </div>
   ```

3. A continuación, añadimos las etiquetas para las tarjetas, asegurándonos de que sean responsivas

   ```html
    <!-- Primera tarjeta -->
               <div class="col-12 col-sm-6 col-md-4 mb-4 d-flex justify-content-center">
                   <div class="card card-custom">
                       <img src="https://via.placeholder.com/150" class="card-img-top" alt="Card Image 1">
                       <div class="card-body">
                           <h5 class="card-title">Card Title 1</h5>
                           <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                           <a href="#" class="btn btn-primary">Go somewhere</a>
                       </div>
                   </div>
               </div>
   ```

   Si deseas agregar más tarjetas, solo necesitas copiar el código anterior y modificar las diferentes opciones según sea necesario.

   # **Explicación del código:**

   ### a. Contenedor Principal:

   ```html
   <div class="container mt-5">
   ```

   `container`: Clase de Bootstrap para centrar y añadir márgenes laterales.
   `mt-5`: Clase de Bootstrap para añadir un margen superior (margin-top).

   

   ### b. Fila para Tarjetas:

   ```html
   <div class="row justify-content-center">
   ```

   `row`: Clase de Bootstrap para crear una fila de columnas.
   `justify-content-center`: Clase de Bootstrap para centrar el contenido horizontalmente.

   

   ### c. Columnas Responsivas:

   ```html
   <div class="col-12 col-sm-6 col-md-4 mb-4 d-flex justify-content-center">
   ```

   `col-12`: Ocupa el ancho completo en pantallas extra pequeñas.
   `col-sm-6`: Ocupa la mitad del ancho en pantallas pequeñas.
   `col-md-4`: Ocupa un tercio del ancho en pantallas medianas y superiores.
   `mb-4`: Añade un margen inferior a cada columna.
   `d-flex justify-content-center`: Utiliza d-flex para hacer que el contenedor de la tarjeta sea un flexbox y justify-content-center para centrar horizontalmente la tarjeta dentro de la columna.

   ### d. Tarjeta con Contenido Mixto:

   ```html
   <div class="col-12 col-sm-6 col-md-4 mb-4 d-flex justify-content-center">
                   <div class="card card-custom">
                       <img src="https://via.placeholder.com/150" class="card-img-top" alt="Card Image 1">
                       <div class="card-body">
                           <h5 class="card-title">Card Title 1</h5>
                           <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                           <a href="#" class="btn btn-primary">Go somewhere</a>
                       </div>
                   </div>
               </div>
   ```

   `card`: Clase de Bootstrap para estilizar el contenedor de la tarjeta.
   `card-custom`: Clase personalizada para definir un ancho fijo de la tarjeta.
   `card-img-top`: Clase de Bootstrap para las imágenes en la parte superior de la tarjeta.
   `card-body`: Clase de Bootstrap para el contenido principal de la tarjeta.
   `card-title`: Clase de Bootstrap para el título de la tarjeta.
   `card-text`: Clase de Bootstrap para el texto de la tarjeta.
   `btn btn-primary`: Clases de Bootstrap para estilizar el botón.

   

   ### e. CSS Personalizado:

   ```css
       <style>
           .card-custom {
               width: 18rem; /* Ancho fijo de la tarjeta */
           }
       </style>
   ```

   `width: 18rem;`: Define un ancho fijo de 18 rem (rem es una unidad relativa en CSS).

   # **Código Completo**

   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
   
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>Responsive Cards</title>
   
       <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
   
       <style>
           .card-custom {
               width: 18rem; /* Ancho fijo de la tarjeta */
           }
       </style>
   
   
   </head>
   
   <body>
   
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
               </ul>
           </div>
       </div>
   </nav>
   
   
       <!-- Contenedor principal -->
       <div class="container mt-5">
           <!-- Fila para contener las tarjetas -->
           <div class="row justify-content-center">
   
   
               <!-- Primera tarjeta -->
               <div class="col-12 col-sm-6 col-md-4 mb-4 d-flex justify-content-center">
                   <div class="card card-custom">
                       <img src="https://via.placeholder.com/150" class="card-img-top" alt="Card Image 1">
                       <div class="card-body">
                           <h5 class="card-title">Card Title 1</h5>
                           <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                           <a href="#" class="btn btn-primary">Go somewhere</a>
                       </div>
                   </div>
               </div>
   
   
   
           </div>
       </div>
   
   
   <!-- Script -->
   <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
   
   </body>
   </html>
   ```

   



