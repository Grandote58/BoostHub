# ![Mesa de trabajo 1Head](http://drive.google.com/uc?export=view&id=1p2rqX0Nck3MI8LKzYct_oEMRETRIhzTH)


# **Contenidos WEB - Mas Profesionales**

En esta práctica, crearemos un contenedor que incluye tres tarjetas, cada una con una imagen, un título, una descripción y un botón. El contenedor estará preparado para recibir más tarjetas, asegurando que todas mantengan las mismas propiedades responsivas y se vean bien en pantallas pequeñas. Utilizaremos márgenes para una adecuada distribución y alineación.

### Pasos a Seguir .!

1. **Incluir Bootstrap CSS desde CDN**

   ```html
   <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
   ```

2. **Incluir nuestra hoja de estilos personalizada**

   ```html
   <link href="styles.css" rel="stylesheet">
   ```

3. **Estructura de las Tarjetas**

   - Cada tarjeta incluye una imagen, un título, una descripción y un botón.
   - Las tarjetas están organizadas en una fila (`row`) y cada tarjeta ocupa una columna (`col-md-4`).

   ```html
   <div class="container my-4">
     <div class="row">
       <!-- Tarjeta 1 -->
       <div class="col-md-4 mb-4">
         <div class="card">
           <img src="image1.jpg" class="card-img-top" alt="Imagen 1">
           <div class="card-body">
             <h5 class="card-title">Título de la Tarjeta 1</h5>
             <p class="card-text">Descripción de la tarjeta 1. Esta es una breve descripción para mostrar el contenido de la tarjeta.</p>
             <a href="#" class="btn btn-primary">Leer Más</a>
           </div>
         </div>
       </div>
       <!-- Tarjeta 2 -->
       <div class="col-md-4 mb-4">
         <div class="card">
           <img src="image2.jpg" class="card-img-top" alt="Imagen 2">
           <div class="card-body">
             <h5 class="card-title">Título de la Tarjeta 2</h5>
             <p class="card-text">Descripción de la tarjeta 2. Esta es una breve descripción para mostrar el contenido de la tarjeta.</p>
             <a href="#" class="btn btn-primary">Leer Más</a>
           </div>
         </div>
       </div>
       <!-- Tarjeta 3 -->
       <div class="col-md-4 mb-4">
         <div class="card">
           <img src="image3.jpg" class="card-img-top" alt="Imagen 3">
           <div class="card-body">
             <h5 class="card-title">Título de la Tarjeta 3</h5>
             <p class="card-text">Descripción de la tarjeta 3. Esta es una breve descripción para mostrar el contenido de la tarjeta.</p>
             <a href="#" class="btn btn-primary">Leer Más</a>
           </div>
         </div>
       </div>
     </div>
     <!-- Colocar aquí más tarjetas -->
     <div class="row">
       <!-- Ejemplo de otra tarjeta -->
       <div class="col-md-4 mb-4">
         <div class="card">
           <img src="image4.jpg" class="card-img-top" alt="Imagen 4">
           <div class="card-body">
             <h5 class="card-title">Título de la Tarjeta 4</h5>
             <p class="card-text">Descripción de la tarjeta 4. Esta es una breve descripción para mostrar el contenido de la tarjeta.</p>
             <a href="#" class="btn btn-primary">Leer Más</a>
           </div>
         </div>
       </div>
     </div>
   </div>
   ```

4. **Incluir Bootstrap JS desde CDN**

   ```html
   <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
   ```

### Explicación y Personalización

1. **Imágenes Responsivas en las Tarjetas**
   - La clase `card-img-top` asegura que las imágenes sean responsivas y se ajusten correctamente a diferentes tamaños de pantalla.
   - La propiedad `object-fit: cover;` asegura que las imágenes cubran completamente el área de la tarjeta sin distorsionarse.
2. **Márgenes y Alineación de las Tarjetas**
   - La clase `card` incluye márgenes, bordes redondeados y una sombra para mejorar la apariencia de las tarjetas.
   - La clase `card-body` asegura que el contenido de las tarjetas esté centrado y bien alineado.

### Actividades de Mejora para las Tarjetas

1. **Agregar Efectos de Hover:**
   - Permitir que el estudiante agregue efectos de hover a las tarjetas utilizando CSS para mejorar la interactividad.
2. **Implementar Animaciones:**
   - Añadir animaciones a las tarjetas y a los botones para mejorar la experiencia del usuario.
3. **Personalización del Tema:**
   - Crear un selector de temas que permita a los usuarios cambiar entre diferentes esquemas de color para las tarjetas.
4. **Optimización para Dispositivos Móviles:**
   - Asegurarse de que las tarjetas se vean bien en todos los tamaños de pantalla, haciendo ajustes necesarios en el CSS.

### Código Completo

#### Paso 1: Crear la Estructura HTML

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Práctica: Tarjetas Responsivas</title>
  <!-- Incluimos el CSS de Bootstrap desde CDN -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
  <!-- Incluimos nuestra hoja de estilos personalizada -->
  <link href="styles.css" rel="stylesheet">
</head>
<body>
  <div class="container my-4">
    <div class="row">
      <!-- Tarjeta 1 -->
      <div class="col-md-4 mb-4">
        <div class="card">
          <img src="image1.jpg" class="card-img-top" alt="Imagen 1">
          <div class="card-body">
            <h5 class="card-title">Título de la Tarjeta 1</h5>
            <p class="card-text">Descripción de la tarjeta 1. Esta es una breve descripción para mostrar el contenido de la tarjeta.</p>
            <a href="#" class="btn btn-primary">Leer Más</a>
          </div>
        </div>
      </div>
      <!-- Tarjeta 2 -->
      <div class="col-md-4 mb-4">
        <div class="card">
          <img src="image2.jpg" class="card-img-top" alt="Imagen 2">
          <div class="card-body">
            <h5 class="card-title">Título de la Tarjeta 2</h5>
            <p class="card-text">Descripción de la tarjeta 2. Esta es una breve descripción para mostrar el contenido de la tarjeta.</p>
            <a href="#" class="btn btn-primary">Leer Más</a>
          </div>
        </div>
      </div>
      <!-- Tarjeta 3 -->
      <div class="col-md-4 mb-4">
        <div class="card">
          <img src="image3.jpg" class="card-img-top" alt="Imagen 3">
          <div class="card-body">
            <h5 class="card-title">Título de la Tarjeta 3</h5>
            <p class="card-text">Descripción de la tarjeta 3. Esta es una breve descripción para mostrar el contenido de la tarjeta.</p>
            <a href="#" class="btn btn-primary">Leer Más</a>
          </div>
        </div>
      </div>
    </div>
    <!-- Colocar aquí más tarjetas -->
    <div class="row">
      <!-- Ejemplo de otra tarjeta -->
      <div class="col-md-4 mb-4">
        <div class="card">
          <img src="image4.jpg" class="card-img-top" alt="Imagen 4">
          <div class="card-body">
            <h5 class="card-title">Título de la Tarjeta 4</h5>
            <p class="card-text">Descripción de la tarjeta 4. Esta es una breve descripción para mostrar el contenido de la tarjeta.</p>
            <a href="#" class="btn btn-primary">Leer Más</a>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Incluimos el JS de Bootstrap desde CDN -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
</body>
</html>
```

#### Paso 2: Crear la Hoja de Estilos CSS

```css
/* styles.css */
/* Estilo para las imágenes de las tarjetas */
.card-img-top {
  width: 100%;
  height: auto;
  object-fit: cover;
}

/* Márgenes y alineación de las tarjetas */
.card {
  margin: 0 auto;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.card-body {
  text-align: center;
}
```

### Actividad de Evaluación

1. **Objetivo:**
   - Evaluar la capacidad del estudiante para personalizar las tarjetas, añadir nuevas características y asegurar que todo el contenido sea completamente responsivo.
2. **Instrucciones:**
   - Implementar al menos tres de las mejoras sugeridas anteriormente.
   - Documentar los cambios realizados y explicar cómo cada mejora mejora la usabilidad y la experiencia del usuario.


# ![Mesa de trabajo 1FOOTER](http://drive.google.com/uc?export=view&id=1vwLVsNlcF2PEyv9fULe2cohQnVfwRWLg)
