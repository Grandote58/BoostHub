# ![Mesa de trabajo 1Head](http://drive.google.com/uc?export=view&id=1p2rqX0Nck3MI8LKzYct_oEMRETRIhzTH)


# **Contenidos WEB - Mas Profesionales**

### Práctica: Creación de un Menú Responsivo con Navbar de Bootstrap

En esta práctica, crearemos un menú de navegación responsivo utilizando la instrucción `navbar` de Bootstrap, HTML5 y CSS. El menú incluirá las opciones "Home", "Misión", "Productos" (con submenús "Producto 1" y "Producto 2") y "Contacto". El logo responsivo de 60x60 y el nombre de la empresa estarán dentro del `navbar`. Además, se personalizarán el fondo y el color de las letras del menú, y se incluirá un icono de WhatsApp en la opción de contacto utilizando Bootstrap Icons. El menú se convertirá en un menú hamburguesa en pantallas pequeñas para asegurar que todo el contenido sea responsivo.

#### Pasos a Tener Encuenta!

1. **Incluir Bootstrap CSS desde CDN**

   ```html
   <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
   ```

2. **Incluir Bootstrap Icons desde CDN**

   ```html
   <link href="https://cdn.jsdelivr.net/npm/bootstrap-icons/font/bootstrap-icons.css" rel="stylesheet">
   ```

3. **Incluir nuestra hoja de estilos personalizada**

   ```html
   <link href="styles.css" rel="stylesheet">
   ```

4. **Crear el contenedor principal del navbar**

   ```html
   <nav class="navbar navbar-expand-lg navbar-light bg-custom">
     <div class="container-fluid">
   ```

5. **Agregar el logo y el nombre de la empresa dentro del navbar**

   ```html
   <a class="navbar-brand d-flex align-items-center" href="#">
     <img src="logo.png" alt="Logo" class="logo">
     <span class="company-name">Nombre de la Empresa</span>
   </a>
   ```

6. **Botón de menú hamburguesa para pantallas pequeñas**

   ```html
   <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
     <span class="navbar-toggler-icon"></span>
   </button>
   ```

7. **Contenido del menú**

   ```html
   <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
     <ul class="navbar-nav">
       <li class="nav-item">
         <a class="nav-link" href="#">Home</a>
       </li>
       <li class="nav-item">
         <a class="nav-link" href="#">Misión</a>
       </li>
       <li class="nav-item dropdown">
         <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">
           Productos
         </a>
         <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
           <li><a class="dropdown-item" href="#">Producto 1</a></li>
           <li><a class="dropdown-item" href="#">Producto 2</a></li>
         </ul>
       </li>
       <li class="nav-item">
         <a class="nav-link" href="#"><i class="bi bi-whatsapp"></i> Contacto</a>
       </li>
     </ul>
   </div>
   ```

8. **Cerrar contenedor principal del navbar**

   ```html
       </div>
   </nav>
   ```

9. **Incluir Bootstrap JS desde CDN**

   ```html
   <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha3
   ```

### Solución Completa

#### Paso 1: Crear la Estructura HTML

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Menú Responsivo</title>
  <!-- Incluimos el CSS de Bootstrap desde CDN -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
  <!-- Incluimos los iconos de Bootstrap desde CDN -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap-icons/font/bootstrap-icons.css" rel="stylesheet">
  <!-- Incluimos nuestra hoja de estilos personalizada -->
  <link href="styles.css" rel="stylesheet">
</head>
<body>
  <nav class="navbar navbar-expand-lg navbar-light bg-custom">
    <div class="container-fluid">
      <!-- Logo y nombre de la empresa dentro del navbar -->
      <a class="navbar-brand d-flex align-items-center" href="#">
        <img src="logo.png" alt="Logo" class="logo">
        <span class="company-name">Nombre de la Empresa</span>
      </a>
      <!-- Botón de menú hamburguesa para pantallas pequeñas -->
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <!-- Contenido del menú -->
      <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link" href="#">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Misión</a>
          </li>
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">
              Productos
            </a>
            <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
              <li><a class="dropdown-item" href="#">Producto 1</a></li>
              <li><a class="dropdown-item" href="#">Producto 2</a></li>
            </ul>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#"><i class="bi bi-whatsapp"></i> Contacto</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- Incluimos el JS de Bootstrap desde CDN -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
</body>
</html>
```

#### Paso 2: Crear la Hoja de Estilos CSS

```css
/* styles.css */
/* Estilo para el logo */
.logo {
  width: 60px;
  height: 60px;
}

/* Estilo para el nombre de la empresa */
.company-name {
  font-size: 1.5em;
  margin-left: 10px;
}

/* Personalizar el fondo y color del navbar */
.bg-custom {
  background-color: #343a40;
}

.navbar-nav .nav-link {
  color: #ffffff;
}

.navbar-nav .nav-link:hover {
  color: #adb5bd;
}
```

### Resultado Final

Este código proporcionado crea un menú de navegación responsivo utilizando la instrucción `navbar` de Bootstrap. El menú incluye las opciones "Home", "Misión", "Productos" (con submenús "Producto 1" y "Producto 2") y "Contacto", con un icono de WhatsApp en la opción de contacto. El logo y el nombre de la empresa se muestran de forma adecuada y responsiva dentro del `navbar`. Cuando el tamaño de la pantalla se reduce, el menú se convierte en un menú hamburguesa utilizando las clases de Bootstrap. El fondo y el color de las letras del menú se personalizan mediante la hoja de estilos. Todo el contenido es responsivo y se ajusta a diferentes tamaños de pantalla utilizando las características de Bootstrap.

Este ejemplo puede servir como base para crear menús más complejos y adaptativos, mejorando la experiencia del usuario en diferentes dispositivos.



# ![Mesa de trabajo 1FOOTER](http://drive.google.com/uc?export=view&id=1vwLVsNlcF2PEyv9fULe2cohQnVfwRWLg)
