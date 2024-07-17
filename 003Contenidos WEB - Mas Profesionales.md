# ![Mesa de trabajo 1Head](http://drive.google.com/uc?export=view&id=1p2rqX0Nck3MI8LKzYct_oEMRETRIhzTH)

# **Contenidos WEB - Mas Profesionales**

En esta práctica, crearemos un header responsivo que incluye una imagen que puede redimensionarse tanto en ancho como en alto, y títulos principales y secundarios junto con un botón. Los textos y el botón podrán colocarse en cualquier parte del header y tendrán un fondo transparente. También se asegurarán de que todo el contenido sea responsivo y se vea bien en pantallas pequeñas.

### Pasos a Seguir .!

1. **Incluir Bootstrap CSS desde CDN**

   ```html
   <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
   ```

2. **Incluir nuestra hoja de estilos personalizada**

   ```html
   <link href="styles.css" rel="stylesheet">
   ```

3. **Estructura del Header**

   - Incluye una imagen responsiva, títulos y botón que pueden redimensionarse y colocarse en cualquier parte del header.

   ```html
   <!-- Header con imagen y contenido -->
   <header class="header">
     <img src="header-image.jpg" alt="Header Image" class="header-img">
     <div class="header-content">
       <h1 class="main-title">Nombre de La Empresa</h1>
       <h2 class="sub-title">Esto es fascinante</h2>
       <button class="btn btn-primary">Leer Más</button>
     </div>
   </header>
   ```

4. **Incluir Bootstrap JS desde CDN**

   ```html
   <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
   ```

### Explicación y Personalización

1. **Imagen Responsiva en el Header**
   - La clase `header-img` asegura que la imagen sea responsiva y se ajuste correctamente a diferentes tamaños de pantalla.
   - La propiedad `object-fit: cover;` asegura que la imagen cubra completamente el área del header sin distorsionarse.
2. **Contenido del Header**
   - La clase `header-content` utiliza `position: absolute;` para colocar el contenido en cualquier parte del header.
   - La propiedad `transform: translate(-50%, -50%);` centra el contenido tanto horizontal como verticalmente.
   - El fondo semitransparente se logra con `background-color: rgba(0, 0, 0, 0.5);`, proporcionando un contraste legible contra la imagen del header.
3. **Textos y Botón**
   - Las clases `main-title` y `sub-title` definen los tamaños de fuente y márgenes para los títulos principal y secundario.
   - La clase `btn` dentro de `header-content` estiliza el botón, haciendo que se vea prominente y accesible.

### Actividades de Mejora para el Header

1. **Agregar Efectos de Desplazamiento:**
   - Permitir que el estudiante agregue efectos de desplazamiento a los elementos del header utilizando CSS o JavaScript.
2. **Implementar Animaciones:**
   - Añadir animaciones a los textos y al botón para mejorar la experiencia del usuario.
3. **Personalización del Tema:**
   - Crear un selector de temas que permita a los usuarios cambiar entre diferentes esquemas de color para el header y los textos.
4. **Optimización para Dispositivos Móviles:**
   - Asegurarse de que el contenido del header se vea bien en todos los tamaños de pantalla, haciendo ajustes necesarios en el CSS.

### Código Completo.

#### Paso 1: Crear la Estructura HTML

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Práctica: Header Responsivo</title>
  <!-- Incluimos el CSS de Bootstrap desde CDN -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
  <!-- Incluimos nuestra hoja de estilos personalizada -->
  <link href="styles.css" rel="stylesheet">
</head>
<body>
  <!-- Header con imagen y contenido -->
  <header class="header">
    <img src="header-image.jpg" alt="Header Image" class="header-img">
    <div class="header-content">
      <h1 class="main-title">Nombre de La Empresa</h1>
      <h2 class="sub-title">Esto es fascinante</h2>
      <button class="btn btn-primary">Leer Más</button>
    </div>
  </header>

  <!-- Incluimos el JS de Bootstrap desde CDN -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
</body>
</html>
```

#### Paso 2: Crear la Hoja de Estilos CSS

```css
/* styles.css */
/* Estilo para la imagen del header */
.header-img {
  width: 100%;
  height: auto;
  max-height: 400px; /* Ajuste de altura máxima */
  object-fit: cover; /* Ajuste para que la imagen se ajuste correctamente */
}

/* Estilos para el contenido del header */
.header {
  position: relative;
  text-align: center;
  color: #ffffff;
}

.header-content {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background-color: rgba(0, 0, 0, 0.5); /* Fondo semitransparente */
  padding: 20px;
  border-radius: 10px;
}

.main-title {
  font-size: 2.5em;
  margin-bottom: 10px;
}

.sub-title {
  font-size: 1.5em;
  margin-bottom: 20px;
}

/* Estilos para el botón */
.header-content .btn {
  font-size: 1.2em;
}
```

### Actividad de Evaluación

1. **Objetivo:**
   - Evaluar la capacidad del estudiante para personalizar el header, añadir nuevas características y asegurar que todo el contenido sea completamente responsivo.
2. **Instrucciones:**
   - Implementar al menos tres de las mejoras sugeridas anteriormente.
   - Documentar los cambios realizados y explicar cómo cada mejora mejora la usabilidad y la experiencia del usuario.

# ![Mesa de trabajo 1FOOTER](http://drive.google.com/uc?export=view&id=1vwLVsNlcF2PEyv9fULe2cohQnVfwRWLg)
