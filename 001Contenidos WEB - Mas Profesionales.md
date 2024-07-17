# ![Mesa de trabajo 1Head](http://drive.google.com/uc?export=view&id=1p2rqX0Nck3MI8LKzYct_oEMRETRIhzTH)

# **Contenidos WEB - Mas Profesionales**

### Practica 001 : Plantilla de HTML5 con Grid System

**Objetivo:** Crear una plantilla de HTML5 que incluya `header`, `nav`, `section`, `aside` y `footer`, cada uno con una tabla de una fila y una columna de color diferente, utilizando el **Grid system** para hacerla responsiva.

![image-20240716122120877](C:\Users\juanc\AppData\Roaming\Typora\typora-user-images\image-20240716122120877.png)



#### Paso 1: Estructura HTML

Crea un archivo llamado `index.html` y agrega la siguiente estructura:

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Plantilla HTML5 con Grid System</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <table>
            <tr>
                <td>Header</td>
            </tr>
        </table>
    </header>
    <nav>
        <table>
            <tr>
                <td>Nav</td>
            </tr>
        </table>
    </nav>
    <div class="container">
        <section>
            <table>
                <tr>
                    <td>Section</td>
                </tr>
            </table>
        </section>
        <aside>
            <table>
                <tr>
                    <td>Aside</td>
                </tr>
            </table>
        </aside>
    </div>
    <footer>
        <table>
            <tr>
                <td>Footer</td>
            </tr>
        </table>
    </footer>
</body>
</html>
```

#### Paso 2: Estilos CSS con Grid System

Crea un archivo llamado `styles.css` y agrega los siguientes estilos:

```css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    display: grid;
    grid-template-rows: auto 1fr auto;
    grid-template-columns: 1fr;
    min-height: 100vh;
}

header {
    background-color: #4CAF50;
    padding: 10px;
    text-align: center;
    grid-column: 1 / -1;
}

nav {
    background-color: #333;
    color: white;
    text-align: center;
    grid-column: 1 / -1;
}

.container {
    display: grid;
    grid-template-columns: 1fr;
    gap: 10px;
    padding: 10px;
}

section {
    background-color: #f1f1f1;
    padding: 10px;
}

aside {
    background-color: #ffeb3b;
    padding: 10px;
}

footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 10px;
    grid-column: 1 / -1;
}

table {
    width: 100%;
    height: 100px;
}

td {
    text-align: center;
    vertical-align: middle;
}

/* Responsive Design */
@media (min-width: 600px) {
    .container {
        grid-template-columns: 2fr 1fr;
    }

    section {
        grid-column: 1 / 2;
    }

    aside {
        grid-column: 2 / 3;
    }
}
```

#### Explicación

1. **HTML5:**
   - Se define una estructura básica con las etiquetas `<header>`, `<nav>`, `<section>`, `<aside>` y `<footer>`.
   - Cada sección contiene una tabla de una fila y una columna para diferenciar visualmente cada parte.
2. **CSS3 con Grid System:**
   - **Grid Layout:** El `body` se configura como un contenedor de cuadrícula con tres filas (`grid-template-rows`) y una columna (`grid-template-columns`).
   - **Secciones:** Se especifican estilos de fondo y relleno para cada sección (`header`, `nav`, `section`, `aside`, `footer`).
   - **Container:** Dentro de `.container`, se utiliza `grid-template-columns` para definir las columnas de la cuadrícula y `gap` para el espacio entre las columnas.
   - **Responsive Design:** Se utiliza una media query (`@media`) para cambiar el diseño de la cuadrícula cuando el ancho de la pantalla es de al menos 600px, estableciendo dos columnas para `.container`.

### Práctica Adicional

- Cambia los colores y el contenido de las tablas.
- Añade más secciones y personaliza el diseño responsivo.
- Explora propiedades avanzadas de Grid como `grid-area`.


# ![Mesa de trabajo 1FOOTER](http://drive.google.com/uc?export=view&id=1vwLVsNlcF2PEyv9fULe2cohQnVfwRWLg)
