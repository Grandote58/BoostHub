# **Actividad Práctica: **

## **Comprensión y Aplicación de Extensiones en Visual Studio Code con Bootstrap 5**

## **Objetivo de aprendizaje:**

Adquirir un entendimiento profundo de las siguientes extensiones de Visual Studio Code, y aplicarlas en la creación de dos aplicaciones web mediante el uso de **HTML5**, **CSS3** y **Bootstrap 5**.

**Extensiones a utilizar:**

- **Prettier**
- **Live Server**
- **Better Comments**
- **vscode-icons**
- **HTML CSS Support**
- **IntelliSense for CSS**
- **CSS Peek**
- **JavaScript (ES6) code snippets**
- **Indent-rainbow**
- **Path Intellisense**
- **Image Preview**
- **vscode-pets**
- **Auto Rename Tag**
- **Bootstrap 5 Snippets**
- **Bootstrap 5 & Font Awesome Snippets**

------

### **Parte 1: Investigación de Extensiones**

1. **Averiguación:** Investiga el concepto, funcionamiento, y proceso de instalación de cada extensión listada.
2. **Documentación:** Elabora un documento donde expliques de manera breve y clara la utilidad de cada extensión y cómo se integra en un entorno de desarrollo web.

------

### **Parte 2: Desarrollo de Proyectos Web**

Los equipos desarrollarán **dos aplicaciones web**, utilizando las extensiones y herramientas investigadas. A continuación, se presentan los detalles para cada proyecto:

------

#### **Aplicación 1: Web sobre Béisbol**

- **Tema:** Crear una página web relacionada con el béisbol, con 3 secciones: Inicio, Equipos, y Contacto.
- Requisitos técnicos:
  - Implementar una **barra de navegación** con **Bootstrap 5** para enlazar las 3 páginas.
  - Utilizar **imágenes** y **contenido informativo** sobre equipos o jugadores.
  - Navegación funcional entre las páginas.

------

#### **Aplicación 2: Web sobre Historia Colombiana**

- **Tema:** Crear una página web con 3 secciones: Inicio, Historia, y Contacto, sobre un aspecto relevante de la historia de Colombia.
- Requisitos técnicos:
  - Incluir una barra de navegación con **Bootstrap 5**.
  - Cada página debe contener información relevante sobre el tema seleccionado, imágenes ilustrativas y navegación funcional.

------

### **Parte 3: Ejemplos de Código**

**1. Ejemplo de Barra de Navegación con Bootstrap 5:**

```html
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <div class="container-fluid">
    <a class="navbar-brand" href="index.html">Mi Sitio</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item">
          <a class="nav-link active" href="index.html">Inicio</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="equipos.html">Equipos</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="contacto.html">Contacto</a>
        </li>
      </ul>
    </div>
  </div>
</nav>
```

**2. Hipervínculos en las páginas:** Asegúrate de que cada sección de la página tenga hipervínculos que naveguen entre las páginas de tu aplicación web.

```html
<a href="index.html">Volver al Inicio</a>
<a href="equipos.html">Ver Equipos</a>
<a href="contacto.html">Contáctanos</a>
```

------

### **Parte 4: Estructura de Archivos**

Asegúrate de seguir la siguiente estructura para ambos proyectos:

```scss
project-name/
│
├── index.html
├── equipos.html (o historia.html para la segunda aplicación)
├── contacto.html
│
├── css/
│   └── styles.css (hoja de estilo personalizada)
│
├── img/
│   └── (imágenes utilizadas en la aplicación)
│
└── js/
    └── main.js (si es necesario para interactividad adicional)
```

------

### **Parte 5: Entregables**

1. **Documento** con la explicación de las extensiones utilizadas.
2. Los archivos de ambas aplicaciones web desarrolladas, con el código bien comentado y documentado, entrega los proyectos en un archivo .ZIP o .RAR.
3. **Trabajo en equipos de tres personas** para fomentar la colaboración y el aprendizaje grupal.
4. Fecha de entrega, esta será orientada por el Entrenador

------

### **Recursos adicionales:**

- Utiliza **Live Server** para visualizar los cambios en tiempo real.
- **Prettier** y **Better Comments** te ayudarán a mantener tu código limpio y organizado.