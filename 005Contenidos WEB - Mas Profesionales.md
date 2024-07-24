# ![Mesa de trabajo 1Head](http://drive.google.com/uc?export=view&id=1p2rqX0Nck3MI8LKzYct_oEMRETRIhzTH)


# **Contenidos WEB - Mas Profesionales**

## Creación de un Footer Responsivo con Bootstrap

### Objetivos

1. Configurar el espacio para que el contenido pueda ser observado en pantallas pequeñas.
2. Incluir la instrucción `footer` de Bootstrap para estructurar el contenido del footer de manera efectiva.

### Paso a Paso

#### Paso 1: Configurar el Espacio para el Footer

Para asegurar que el contenido del footer sea responsivo y se vea correctamente en pantallas pequeñas, utilizaremos las clases de Bootstrap que proporcionan un diseño flexible.

#### Paso 2: Incluir la Instrucción Footer de Bootstrap

```html
<footer class="footer bg-light py-4">
  <div class="container">
    <!-- Contenido del footer irá aquí -->
  </div>
</footer>
```

En este paso, hemos añadido la estructura básica del footer utilizando la clase `footer` de Bootstrap y un contenedor `container` para organizar el contenido.

#### Paso 3: Crear un Contenedor para el Logo de la Empresa

```html
<div class="logo-footer mb-3">
  <img src="logo.png" alt="Logo Empresa" class="logo-img">
</div>
```

#### 

```css
.logo-footer {
  text-align: center;
}

.logo-img {
  width: 80px;
  height: 80px;
}
```

#### Paso 4: Crear un Contenedor para Redes Sociales

```html
<div class="redesocial-footer mb-3">
  <a href="#"><i class="bi bi-facebook"></i></a>
  <a href="#"><i class="bi bi-instagram"></i></a>
  <a href="#"><i class="bi bi-linkedin"></i></a>
  <a href="#"><i class="bi bi-tiktok"></i></a>
</div>
```

#### 

```css
.redesocial-footer {
  text-align: center;
}

.redesocial-footer .bi {
  font-size: 1.5em;
  margin: 0 10px;
  color: #ffffff;
}

.redesocial-footer .bi:hover {
  color: #adb5bd;
}
```

#### Paso 5: Crear un Contenedor para Medios de Pago

```html
<div class="mediospago-footer mb-3">
  <i class="bi bi-credit-card"></i>
  <i class="bi bi-paypal"></i>
  <i class="bi bi-mastercard"></i>
  <i class="bi bi-cc-amex"></i>
</div>
```

```css
.mediospago-footer {
  text-align: center;
}

.mediospago-footer .bi {
  font-size: 1.5em;
  margin: 0 10px;
  color: #ffffff;
}

.mediospago-footer .bi:hover {
  color: #adb5bd;
}
```

#### Paso 6: Crear un Contenedor Interno para Información

```html
<div class="contenedorinterno-footer p-3 mb-3">
  <table class="table table-borderless text-center tabla-footer">
    <thead>
      <tr>
        <th>Contacto</th>
        <th>Categorías Principales</th>
        <th>Cotizaciones</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>info@empresa.com</td>
        <td>Electrónica</td>
        <td>Envíos Rápidos</td>
      </tr>
      <tr>
        <td>+123 456 7890</td>
        <td>Moda</td>
        <td>Calidad Garantizada</td>
      </tr>
      <tr>
        <td>Dirección</td>
        <td>Hogar</td>
        <td>Mejores Precios</td>
      </tr>
      <tr>
        <td>Horario</td>
        <td>Juguetes</td>
        <td>Atención Personalizada</td>
      </tr>
      <tr>
        <td>FAQ</td>
        <td>Deportes</td>
        <td>Ofertas Exclusivas</td>
      </tr>
    </tbody>
  </table>
</div>
```

#### 

```css
.contenedorinterno-footer {
  background-color: #006400;
  border-radius: 10px;
  color: #ffffff;
}

.tabla-footer th, .tabla-footer td {
  background-color: transparent;
  color: #ffffff;
}

.tabla-footer th {
  text-align: center;
}
```

#### Paso 7: Agregar Texto de Copyright

```html
<div class="text-center mt-3">
  <p>Copyright 2022 | Website by Empower</p>
</div>
```

```css
footer p {
  margin: 0;
  color: #ffffff;
  font-size: 0.9em;
}
```

#### Paso 8: Incluir Bootstrap desde CDN

##### Enlace CSS de Bootstrap

```html
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
```

##### Enlace JS de Bootstrap

```html
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
```

### Resultado Final

El código final incluye un footer bien estructurado y personalizable. Aquí está el código completo del HTML y CSS.

#### HTML Completo

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Práctica: Footer Responsivo</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
  <link href="styles.css" rel="stylesheet">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap-icons/font/bootstrap-icons.css" rel="stylesheet">
</head>
<body>
  <footer class="fondo-footer py-4">
    <div class="container text-center">
      <div class="logo-footer mb-3">
        <img src="logo.png" alt="Logo Empresa" class="logo-img">
      </div>
      <div class="redesocial-footer mb-3">
        <a href="#"><i class="bi bi-facebook"></i></a>
        <a href="#"><i class="bi bi-instagram"></i></a>
        <a href="#"><i class="bi bi-linkedin"></i></a>
        <a href="#"><i class="bi bi-tiktok"></i></a>
      </div>
      <div class="mediospago-footer mb-3">
        <i class="bi bi-credit-card"></i>
        <i class="bi bi-paypal"></i>
        <i class="bi bi-mastercard"></i>
        <i class="bi bi-cc-amex"></i>
      </div>
      <div class="contenedorinterno-footer p-3 mb-3">
        <table class="table table-borderless text-center tabla-footer">
          <thead>
            <tr>
              <th>Contacto</th>
              <th>Categorías Principales</th>
              <th>Cotizaciones</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>info@empresa.com</td>
              <td>Electrónica</td>
              <td>Envíos Rápidos</td>
            </tr>
            <tr>
              <td>+123 456 7890</td>
              <td>Moda</td>
              <td>Calidad Garantizada</td>
            </tr>
            <tr>
              <td>Dirección</td>
              <td>Hogar</td>
              <td>Mejores Precios</td>
            </tr>
            <tr>
              <td>Horario</td>
              <td>Juguetes</td>
              <td>Atención Personalizada</td>
            </tr>
            <tr>
              <td>FAQ</td>
              <td>Deportes</td>
              <td>Ofertas Exclusivas</td>
            </tr>
          </tbody>
        </table>
      </div>
      <div class="text-center mt-3">
        <p>Copyright 2022 | Website by Empower</p>
      </div>
    </div>
  </footer>
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
</body>
</html>
```

#### CSS Completo

```
cssCopiar código/* styles.css */
/* Fondo del footer con degradado y transparencia, alineado a la izquierda */
.fondo-footer {
  background: linear-gradient(to right, rgba(0, 0, 0, 0.8), rgba(0, 0, 0, 0.5));
  text-align: left;
  color: #ffffff;
}

/* Estilo para el logo del footer */
.logo-footer {
  text-align: center;
}

.logo-img {
  width: 80px;
  height: 80px;
}

/* Estilo para los iconos de redes sociales */
.redesocial-footer {
  text-align: center;
}

.redesocial-footer .bi {
  font-size: 1.5em;
  margin: 0 10px;
  color: #ffffff;
}

.redesocial-footer .bi:hover {
  color: #adb5bd;
}

/* Estilo para los iconos de medios de pago */
.mediospago-footer {
  text-align: center;
}

.mediospago-footer .bi {
  font-size: 1.5em;
  margin: 0 10px;
  color: #ffffff;
}

.mediospago-footer .bi:hover {
  color: #adb5bd;
}

/* Estilo para el contenedor de información */
.contenedorinterno-footer {
  background-color: #006400;
  border-radius: 10px;
  color: #ffffff;
}

.tabla-footer th, .tabla-footer td {
  background-color: transparent;
  color: #ffffff;
}

.tabla-footer th {
  text-align: center;
}

/* Estilo para el texto de copyright */
footer p {
  margin: 0;
  color: #ffffff;
  font-size: 0.9em;
  text-align: center;
}
```



# ![Mesa de trabajo 1FOOTER](http://drive.google.com/uc?export=view&id=1vwLVsNlcF2PEyv9fULe2cohQnVfwRWLg)



