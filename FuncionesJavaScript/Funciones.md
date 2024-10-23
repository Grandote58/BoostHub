# Funciones

Una **función** es un bloque de código que se puede definir una vez y ejecutar (o invocar) en cualquier momento. Las funciones permiten encapsular un conjunto de instrucciones que pueden ser reutilizadas en diferentes partes del programa. 

Estas funciones pueden recibir **parámetros** (datos de entrada) y devolver un **valor** (resultado de la ejecución).

### Estructura de una función en JavaScript:

1. **Declaración de la función**: Se utiliza la palabra clave `function` seguida del nombre de la función, los parámetros entre paréntesis, y el bloque de código entre llaves `{}`.
2. **Invocación de la función**: Se llama a la función por su nombre seguido de paréntesis. Si la función tiene parámetros, se pasan dentro de los paréntesis al invocarla.

#### Ejemplo básico de función:

```javascript
function saludar(nombre) {
    return "Hola, " + nombre + "!";
}

// Invocar la función
const mensaje = saludar("Carlos");
console.log(mensaje);  // Output: "Hola, Carlos!"
```

### Componentes principales:

- **`function`**: Palabra reservada para declarar una función.
- **`nombre`**: El nombre que se le da a la función para identificarla.
- **`nombre` en el parámetro**: Son los datos que la función necesita para trabajar (en este caso, el nombre).
- **`return`**: Palabra reservada que indica el valor que la función devolverá cuando se ejecute.

### Tipos de funciones en JavaScript:

1. **Funciones declaradas**: Son las funciones que se declaran con la palabra clave `function`, como en el ejemplo anterior.

2. **Funciones anónimas:** No tienen un nombre y generalmente se asignan a una variable o se usan como parámetros en otras funciones:

   ```javascript
   const saludar = function(nombre) {
       return "Hola, " + nombre;
   };
   ```

3. **Funciones flecha (arrow functions):** Son una sintaxis más corta para escribir funciones:

   ```javascript
   const saludar = (nombre) => "Hola, " + nombre;
   ```

Las funciones son esenciales en JavaScript, ya que permiten modularizar el código y hacerlo más reutilizable y fácil de mantener.



### Colocación del `<script>`

- **Dentro del `<head>`**: Si colocas la etiqueta `<script>` dentro del `<head>`, el archivo JavaScript se cargará antes de que el cuerpo del HTML sea completamente procesado. Es recomendable añadir el atributo `defer` para asegurarse de que el código JavaScript no se ejecute hasta que todo el HTML esté cargado.

  ```html
  <head>
      <script src="miArchivo.js" defer></script>
  </head>
  ```

- **Antes del cierre de la etiqueta `<body>`**: Este es un enfoque común para asegurarse de que el HTML esté completamente cargado antes de ejecutar el JavaScript.

  ```html
  <body>
      <!-- Código HTML -->
      <script src="miArchivo.js"></script>
  </body>
  ```

  

### Práctica 1: **Introducción a las funciones**

**Descripción:** Crear una función simple que sume dos números.

- HTML:

  ```html
  <input type="text" id="num1" placeholder="Número 1">
  <input type="text" id="num2" placeholder="Número 2">
  <button onclick="sumar()">Sumar</button>
  <p id="resultado"></p>
  ```

- JavaScript:

  ```javascript
  function sumar() {
      const numero1 = parseInt(document.getElementById('num1').value);
      const numero2 = parseInt(document.getElementById('num2').value);
      const resultado = numero1 + numero2;
      document.getElementById('resultado').textContent = "Resultado: " + resultado;
  }
  ```

### Práctica 2: **Uso de parámetros en funciones**

**Descripción:** Crear una función que reciba un texto y lo convierta en mayúsculas.

- HTML:

  ```html
  <input type="text" id="texto" placeholder="Introduce texto">
  <button onclick="convertirMayusculas()">Convertir a Mayúsculas</button>
  <p id="textoResultado"></p>
  ```

- JavaScript:

  ```javascript
  function convertirMayusculas() {
      const textoIngresado = document.getElementById('texto').value;
      const textoEnMayusculas = textoIngresado.toUpperCase();
      document.getElementById('textoResultado').textContent = textoEnMayusculas;
  }
  ```

### Práctica 3: **Devolver valores en funciones**

**Descripción:** Crear una función que devuelva el doble de un número introducido por el usuario.

- HTML:

  ```html
  <input type="text" id="numero" placeholder="Introduce un número">
  <button onclick="calcularDoble()">Calcular Doble</button>
  <p id="dobleResultado"></p>
  ```

- JavaScript:

  ```javascript
  function calcularDoble() {
      const numero = parseInt(document.getElementById('numero').value);
      const doble = numero * 2;
      document.getElementById('dobleResultado').textContent = "El doble es: " + doble;
  }
  ```

### Práctica 4: **Funciones anónimas**

**Descripción:** Utilizar una función anónima para saludar al usuario con su nombre.

- HTML:

  ```html
  <input type="text" id="nombre" placeholder="Introduce tu nombre">
  <button id="saludarBtn">Saludar</button>
  <p id="saludoResultado"></p>
  ```

- JavaScript:

  ```javascript
  document.getElementById('saludarBtn').onclick = function() {
      const nombre = document.getElementById('nombre').value;
      document.getElementById('saludoResultado').textContent = "Hola, " + nombre + "!";
  }
  ```

### Práctica 5: **Utilizando Matter.js - Gravedad simple**

**Descripción:** Crear una simulación sencilla de un objeto cayendo utilizando Matter.js.

- HTML:

  ```html
  <button onclick="iniciarSimulacion()">Iniciar Simulación</button>
  <div id="canvasContainer"></div>
  
  <script src="https://cdnjs.cloudflare.com/ajax/libs/matter-js/0.19.0/matter.min.js"></script>
  ```

- JavaScript:

  ```javascript
  function iniciarSimulacion() {
      const Engine = Matter.Engine,
            Render = Matter.Render,
            World = Matter.World,
            Bodies = Matter.Bodies;
  
      const engine = Engine.create();
      const render = Render.create({
          element: document.getElementById('canvasContainer'),
          engine: engine
      });
  
      const suelo = Bodies.rectangle(400, 610, 810, 60, { isStatic: true });
      const bola = Bodies.circle(400, 200, 40, { restitution: 0.9 });
  
      World.add(engine.world, [suelo, bola]);
  
      Engine.run(engine);
      Render.run(render);
  }
  ```

### Práctica 6: **Función con retorno y condicional**

**Descripción:** Crear una función que verifique si un número es par o impar.

- HTML:

  ```html
  <input type="text" id="numeroParImpar" placeholder="Introduce un número">
  <button onclick="verificarParImpar()">Verificar</button>
  <p id="resultadoParImpar"></p>
  ```

- JavaScript:

  ```javascript
  function verificarParImpar() {
      const numero = parseInt(document.getElementById('numeroParImpar').value);
      const resultado = (numero % 2 === 0) ? "Es par" : "Es impar";
      document.getElementById('resultadoParImpar').textContent = resultado;
  }
  ```

### Práctica 7: **Función que genera un objeto**

**Descripción:** Crear una función que devuelva un objeto con los detalles de un usuario.

- HTML:

  ```html
  <input type="text" id="nombreUsuario" placeholder="Nombre">
  <input type="text" id="edadUsuario" placeholder="Edad">
  <button onclick="crearUsuario()">Crear Usuario</button>
  <p id="resultadoUsuario"></p>
  ```

- JavaScript:

  ```javascript
  function crearUsuario() {
      const nombre = document.getElementById('nombreUsuario').value;
      const edad = parseInt(document.getElementById('edadUsuario').value);
      const usuario = {
          nombre: nombre,
          edad: edad
      };
      document.getElementById('resultadoUsuario').textContent = "Usuario creado: " + JSON.stringify(usuario);
  }
  ```

### Práctica 8: **Uso de funciones dentro de otra función**

**Descripción:** Crear dos funciones, una para calcular el área de un rectángulo y otra para mostrar el resultado.

- HTML:

  ```html
  <input type="text" id="base" placeholder="Base">
  <input type="text" id="altura" placeholder="Altura">
  <button onclick="mostrarArea()">Calcular Área</button>
  <p id="areaResultado"></p>
  ```

- JavaScript:

  ```javascript
  function calcularArea(base, altura) {
      return base * altura;
  }
  
  function mostrarArea() {
      const base = parseFloat(document.getElementById('base').value);
      const altura = parseFloat(document.getElementById('altura').value);
      const area = calcularArea(base, altura);
      document.getElementById('areaResultado').textContent = "El área es: " + area;
  }
  ```



# Librería Matter.js

Para incluir Matter.js en tu proyecto, puedes usar el siguiente script para llamarlo directamente desde una CDN. Añádelo en el `<head>` de tu archivo HTML:

```html
<head>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/matter-js/0.19.0/matter.min.js"></script>
</head>
```

Con este código, podrás usar todas las funcionalidades de Matter.js sin necesidad de descargar la librería.

### Simulaciones de Movimientos Físicos

#### 1. **Simulación de Caída Libre**

Este ejemplo simula la caída libre de un objeto, donde un cuerpo es afectado por la gravedad y cae hasta una superficie plana.

- **HTML**:

  ```html
  <button onclick="simulacionCaidaLibre()">Iniciar Caída Libre</button>
  <div id="caidaLibreContainer"></div>
  ```

- **CSS**

  ```css
      <style>
          #caidaLibreContainer {
              width: 800px;
              height: 600px;
              border: 1px solid #ccc;
          }
      </style>
  ```

  

- **JavaScript**:

  ```javascript
  function simulacionCaidaLibre() {
      // Crear los módulos necesarios de Matter.js
      const Engine = Matter.Engine,
            Render = Matter.Render,
            World = Matter.World,
            Bodies = Matter.Bodies;
  
      // Crear un motor físico con gravedad ajustada
      const engine = Engine.create({
          gravity: {
              scale: 0.001  // Escala de gravedad ajustada para simular la caída libre
          }
      });
  
      // Crear un render (gráficos) y vincularlo al contenedor HTML
      const render = Render.create({
          element: document.getElementById('caidaLibreContainer'),
          engine: engine,
          options: {
              width: 800,
              height: 600,
              wireframes: false // Mostrar cuerpos con relleno
          }
      });
  
      // Crear un suelo estático
      const suelo = Bodies.rectangle(400, 580, 810, 40, { 
          isStatic: true, 
          render: { fillStyle: '#2ecc71' } // Color verde para el suelo
      });
  
      // Crear varias bolas que caerán debido a la gravedad
      const bola1 = Bodies.circle(400, 100, 40, { 
          restitution: 0.8, // Rebote medio
          render: { fillStyle: '#e74c3c' } // Bola roja
      });
      const bola2 = Bodies.circle(500, 150, 30, { 
          restitution: 0.9, // Rebote alto
          render: { fillStyle: '#3498db' } // Bola azul
      });
      const bola3 = Bodies.circle(300, 50, 50, { 
          restitution: 0.5, // Rebote bajo
          render: { fillStyle: '#f1c40f' } // Bola amarilla
      });
  
      // Añadir los objetos (suelo y bolas) al mundo
      World.add(engine.world, [suelo, bola1, bola2, bola3]);
  
      // Iniciar el motor y el render
      Engine.run(engine);
      Render.run(render);
  
      // Aplicar una fuerza pequeña inicial para simular una ligera variación en la caída
      Matter.Body.applyForce(bola1, bola1.position, { x: 0.001, y: 0 });
      Matter.Body.applyForce(bola2, bola2.position, { x: -0.001, y: 0 });
  }
  ```

**Descripción:**

- Se utiliza la función `Bodies.circle()` para crear una bola que cae debido a la gravedad.
- El objeto tiene una propiedad `restitution` que simula la elasticidad (rebote) cuando el objeto choca con el suelo.

#### 2. **Simulación de Colisión Elástica**

Este ejemplo simula una colisión elástica entre dos cuerpos que rebotan al chocar entre sí.

- **HTML**:

  ```html
      <button onclick="simulacionColision()">Iniciar Colisión</button>
      <label for="velocidad">Ajustar Velocidad:</label>
      <input type="range" id="velocidad" min="1" max="10" value="5">
      <div id="colisionContainer"></div>
  
  ```

- **CSS**

  ```css
      <style>
          #colisionContainer {
              width: 800px;
              height: 600px;
              border: 1px solid #ccc;
          }
          label {
              font-family: Arial, sans-serif;
              margin-right: 10px;
          }
      </style>
  ```

  

- **JavaScript**:

  ```javascript
  function simulacionColision() {
      const Engine = Matter.Engine,
            Render = Matter.Render,
            World = Matter.World,
            Bodies = Matter.Bodies;
  
      // Crear el motor físico
      const engine = Engine.create();
  
      // Crear el render y vincularlo al contenedor HTML
      const render = Render.create({
          element: document.getElementById('colisionContainer'),
          engine: engine,
          options: {
              width: 800,
              height: 600,
              wireframes: false  // Mostrar las bolas con colores y relleno
          }
      });
  
      // Crear el suelo estático
      const suelo = Bodies.rectangle(400, 580, 810, 50, { 
          isStatic: true,
          render: { fillStyle: '#2ecc71' }  // Color verde para el suelo
      });
  
      // Crear dos bolas con restitución (rebote) alta y colores distintos
      const bola1 = Bodies.circle(200, 200, 40, { 
          restitution: 1,  // Rebote perfecto
          render: { fillStyle: '#e74c3c' }  // Bola roja
      });
      const bola2 = Bodies.circle(600, 200, 40, { 
          restitution: 1,  // Rebote perfecto
          render: { fillStyle: '#3498db' }  // Bola azul
      });
  
      // Añadir las bolas y el suelo al mundo
      World.add(engine.world, [suelo, bola1, bola2]);
  
      // Añadir una fuerza inicial para que las bolas se desplacen una hacia la otra
      const velocidadInicial = document.getElementById("velocidad").value / 10;  // Ajuste de velocidad según el valor del slider
      Matter.Body.setVelocity(bola1, { x: velocidadInicial, y: 0 });
      Matter.Body.setVelocity(bola2, { x: -velocidadInicial, y: 0 });
  
      // Iniciar el motor y el render
      Engine.run(engine);
      Render.run(render);
  }
  ```

**Descripción:**

- Este código simula una colisión elástica entre dos bolas, las cuales se rebotarán al chocar entre sí debido a la propiedad `restitution: 1`, que indica que la colisión es completamente elástica.

#### 3. **Simulación de un Péndulo Simple**

Este ejemplo simula un péndulo simple que oscila bajo la acción de la gravedad.

- **HTML**:

  ```html
  <button onclick="simulacionPendulo()">Iniciar Péndulo</button>
  <div id="penduloContainer"></div>
  <script src="/nombre del script"></script>
  ```

  **CSS**

  ```css
  #penduloContainer {
         width: 800px;
         height: 600px;
         border: 1px solid #ccc;
  }
  ```

  

- **JavaScript**:

  ```javascript
        function simulacionPendulo() {
              const Engine = Matter.Engine,
                  Render = Matter.Render,
                  World = Matter.World,
                  Bodies = Matter.Bodies,
                  Constraint = Matter.Constraint;
  
              // Crear motor de física
              const engine = Engine.create();
  
              // Crear render para mostrar el canvas en el div 'penduloContainer'
              const render = Render.create({
                  element: document.getElementById('penduloContainer'),
                  engine: engine,
                  options: {
                      width: 800,
                      height: 600,
                      wireframes: false // Para mostrar los cuerpos con relleno en lugar de solo contornos
                  }
              });
  
              // Crear el suelo estático (visible en la simulación)
              const suelo = Bodies.rectangle(400, 580, 810, 30, { isStatic: true });
  
              // Crear la bola del péndulo
              const bola = Bodies.circle(400, 300, 40, {
                  density: 0.001, // Controlar la masa del péndulo
                  restitution: 0.9, // Para que rebote ligeramente
                  render: {
                      fillStyle: '#3498db'
                  }
              });
  
              // Punto fijo desde donde cuelga el péndulo
              const puntoFijo = { x: 400, y: 100 };
  
              // Crear la cuerda (restricción) que conecta el punto fijo con la bola
              const cuerda = Constraint.create({
                  pointA: puntoFijo,
                  bodyB: bola,
                  stiffness: 0.9,  // Rigidez de la cuerda
                  length: 200,      // Longitud de la cuerda
                  render: {
                      lineWidth: 4,
                      strokeStyle: '#2ecc71'
                  }
              });
  
              // Añadir el suelo, la bola y la cuerda al mundo físico
              World.add(engine.world, [suelo, bola, cuerda]);
  
              // Añadir una pequeña fuerza inicial para que el péndulo comience a oscilar
              Matter.Body.applyForce(bola, { x: bola.position.x, y: bola.position.y }, { x: 0.15, y: 0 });
  
              // Ejecutar el motor y el render
              Engine.run(engine);
              Render.run(render);
          }
  ```

**Descripción:**

- Esta simulación muestra un péndulo que oscila desde un punto fijo utilizando una restricción (`Constraint`).
- La bola representa la masa del péndulo, y la cuerda es la restricción que define su movimiento.

### Explicación del Código

- **Matter.Engine**: Este módulo crea el motor físico que será responsable de simular las fuerzas y colisiones entre los objetos.
- **Matter.Render**: Se encarga de dibujar los objetos en un lienzo (canvas) HTML5 para visualizar la simulación.
- **Matter.Bodies**: Permite crear los diferentes cuerpos que forman parte de la simulación, como círculos, rectángulos, y polígonos.
- **Matter.World**: Administra todos los cuerpos y restricciones que se añaden a la simulación.
- **Matter.Constraint**: Permite crear restricciones o conexiones entre dos cuerpos, como una cuerda en el caso del péndulo.



### Recomendaciones

- Las simulaciones físicas pueden ser más interesantes si juegas con las propiedades de los objetos, como la `restitution` (elasticidad) o `stiffness` (rigidez en las cuerdas).
- Puedes modificar las posiciones iniciales de los objetos y las longitudes de las cuerdas para experimentar cómo afectan los movimientos.





### 4. **Simulación de Choque Inelástico**

**Descripción:** Simular el choque inelástico entre dos objetos donde no rebotan y se mueven juntos tras el impacto.

HTML

```html
    <button onclick="simulacionChoqueInelastico()">Iniciar Choque Inelástico</button>
    <label for="velocidad">Ajustar Velocidad:</label>
    <input type="range" id="velocidad" min="1" max="10" value="5">
    <div id="choqueInelasticoContainer"></div>
```

CSS

```css
    <style>
        #choqueInelasticoContainer {
            width: 800px;
            height: 600px;
            border: 1px solid #ccc;
        }
        label {
            font-family: Arial, sans-serif;
            margin-right: 10px;
        }
    </style>
```

JavaScript

```javascript
        function simulacionChoqueInelastico() {
            const Engine = Matter.Engine,
                  Render = Matter.Render,
                  World = Matter.World,
                  Bodies = Matter.Bodies,
                  Body = Matter.Body;

            // Crear el motor físico
            const engine = Engine.create();

            // Crear el render y vincularlo al contenedor HTML
            const render = Render.create({
                element: document.getElementById('choqueInelasticoContainer'),
                engine: engine,
                options: {
                    width: 800,
                    height: 600,
                    wireframes: false  // Mostrar las bolas con colores y relleno
                }
            });

            // Crear el suelo estático
            const suelo = Bodies.rectangle(400, 580, 810, 50, { 
                isStatic: true,
                render: { fillStyle: '#2ecc71' }  // Color verde para el suelo
            });

            // Crear dos bolas con restitución (sin rebote) y colores distintos
            const bola1 = Bodies.circle(300, 100, 40, { 
                restitution: 0,  // Sin rebote
                render: { fillStyle: '#e74c3c' }  // Bola roja
            });
            const bola2 = Bodies.circle(500, 100, 40, { 
                restitution: 0,  // Sin rebote
                render: { fillStyle: '#3498db' }  // Bola azul
            });

            // Añadir las bolas y el suelo al mundo
            World.add(engine.world, [suelo, bola1, bola2]);

            // Ajustar la velocidad inicial de las bolas
            const velocidadInicial = document.getElementById("velocidad").value / 10;
            Body.setVelocity(bola1, { x: velocidadInicial, y: 0 });
            Body.setVelocity(bola2, { x: -velocidadInicial, y: 0 });

            // Función para verificar la colisión y fusionar las bolas
            Matter.Events.on(engine, 'collisionStart', function(event) {
                const pairs = event.pairs;

                pairs.forEach(function(pair) {
                    const bodyA = pair.bodyA;
                    const bodyB = pair.bodyB;

                    // Si las bolas colisionan, las fusionamos (se mueven juntas)
                    if ((bodyA === bola1 && bodyB === bola2) || (bodyA === bola2 && bodyB === bola1)) {
                        // Crear un nuevo cuerpo combinado para que las bolas se muevan juntas
                        const cuerpoFusionado = Bodies.rectangle(
                            (bola1.position.x + bola2.position.x) / 2,
                            bola1.position.y,
                            80, 40,  // Fusionando el ancho de ambas bolas
                            { isStatic: false, render: { fillStyle: '#9b59b6' } }  // Color púrpura
                        );

                        // Eliminar las bolas anteriores
                        World.remove(engine.world, bola1);
                        World.remove(engine.world, bola2);

                        // Añadir el cuerpo fusionado al mundo
                        World.add(engine.world, cuerpoFusionado);
                    }
                });
            });

            // Iniciar el motor y el render
            Engine.run(engine);
            Render.run(render);
        }
```



### 5. Simulación de Ley de Hooke (Resorte)

HTML

```html
    <button onclick="simulacionResorte()">Iniciar Simulación de Resorte</button>
    <div id="resorteContainer"></div>
```

CSS

```css
    <style>
        #resorteContainer {
            width: 800px;
            height: 600px;
            border: 1px solid #ccc;
        }
    </style>
```

JavaScript

```javascript
        function simulacionResorte() {
            // Crear los módulos necesarios de Matter.js
            const Engine = Matter.Engine,
                  Render = Matter.Render,
                  World = Matter.World,
                  Bodies = Matter.Bodies,
                  Constraint = Matter.Constraint;

            // Crear el motor físico
            const engine = Engine.create();

            // Crear el render para visualizar la simulación dentro del contenedor HTML
            const render = Render.create({
                element: document.getElementById('resorteContainer'), // Contenedor HTML donde se mostrará la simulación
                engine: engine,
                options: {
                    width: 800,
                    height: 600,
                    wireframes: false,  // Mostrar los cuerpos con relleno de color
                }
            });

            // Crear una bola que actuará como el objeto sujeto al resorte
            const bola = Bodies.circle(400, 300, 40, {
                restitution: 0.9,  // Añadir un pequeño rebote
                render: { fillStyle: '#3498db' }  // Color de la bola
            });

            // Crear un punto fijo que será el anclaje del resorte
            const puntoFijo = { x: 400, y: 100 }; // Coordenadas fijas del anclaje

            // Crear el resorte (una restricción elástica) entre el punto fijo y la bola
            const resorte = Constraint.create({
                pointA: puntoFijo,  // El punto fijo de donde cuelga el resorte
                bodyB: bola,        // El cuerpo (bola) sujeto por el resorte
                stiffness: 0.02,    // Rigidez baja para simular un resorte flexible
                length: 200,        // Longitud del resorte
                render: {
                    lineWidth: 4,   // Grosor de la línea del resorte
                    strokeStyle: '#2ecc71'  // Color verde para la cuerda del resorte
                }
            });

            // Añadir la bola y el resorte al mundo físico
            World.add(engine.world, [bola, resorte]);

            // Aplicar una fuerza inicial en la bola para que el resorte empiece a oscilar
            Matter.Body.applyForce(bola, { x: bola.position.x, y: bola.position.y }, { x: 0.05, y: -0.05 });

            // Iniciar el motor físico y el render para visualizar la simulación
            Engine.run(engine);
            Render.run(render);
        }
```



### 6. Simulación de Colisión con Fricción

**HTML**

```html
    <button onclick="simulacionFriccion()">Iniciar Simulación de Fricción</button>
    <div id="friccionContainer"></div>
```

**CSS**

```css
        #friccionContainer {
            width: 800px;
            height: 600px;
            border: 1px solid #ccc;
        }
```

**JavaScript**

```javascript
        function simulacionFriccion() {
            // Crear los módulos necesarios de Matter.js
            const Engine = Matter.Engine,
                  Render = Matter.Render,
                  World = Matter.World,
                  Bodies = Matter.Bodies,
                  Body = Matter.Body;

            // Crear el motor físico
            const engine = Engine.create();

            // Crear el render para visualizar la simulación dentro del contenedor HTML
            const render = Render.create({
                element: document.getElementById('friccionContainer'),  // Contenedor HTML donde se mostrará la simulación
                engine: engine,
                options: {
                    width: 800,
                    height: 600,
                    wireframes: false  // Mostrar los cuerpos con relleno de color
                }
            });

            // Crear el suelo estático para la simulación
            const suelo = Bodies.rectangle(400, 580, 810, 40, {
                isStatic: true,  // El suelo no se mueve
                render: { fillStyle: '#2ecc71' }  // Color verde para el suelo
            });

            // Crear una bola con fricción, que afectará su movimiento
            const bola = Bodies.circle(200, 100, 40, {
                friction: 0.1,   // Añadir fricción a la bola
                frictionAir: 0.01,  // Añadir una pequeña fricción con el aire
                restitution: 0.7,  // Rebote moderado
                render: { fillStyle: '#e74c3c' }  // Color rojo para la bola
            });

            // Añadir el suelo y la bola al mundo físico
            World.add(engine.world, [suelo, bola]);

            // Aplicar una fuerza inicial para mover la bola horizontalmente
            Body.applyForce(bola, { x: bola.position.x, y: bola.position.y }, { x: 0.05, y: 0 });

            // Iniciar el motor físico y el render para visualizar la simulación
            Engine.run(engine);
            Render.run(render);
        }
```



### 7. Simulación de Tiro Parabólico

**HTML**

```html
    <div class="controls">
        <label for="velocidad">Velocidad inicial:</label>
        <input type="range" id="velocidad" min="5" max="30" value="15">
        <label for="angulo">Ángulo:</label>
        <input type="range" id="angulo" min="10" max="80" value="45">
        <button onclick="simulacionTiroParabolico()">Iniciar Tiro Parabólico</button>
    </div>
    
    <div id="tiroParabolicoContainer"></div>
```

**CSS**

```css
    <style>
        #tiroParabolicoContainer {
            width: 800px;
            height: 600px;
            border: 1px solid #ccc;
        }

        .controls {
            margin-bottom: 10px;
        }
    </style>
```

**JavaScript**

```javascript
        function simulacionTiroParabolico() {
            // Crear los módulos necesarios de Matter.js
            const Engine = Matter.Engine,
                  Render = Matter.Render,
                  World = Matter.World,
                  Bodies = Matter.Bodies,
                  Body = Matter.Body;

            // Crear el motor físico
            const engine = Engine.create();

            // Crear el render para visualizar la simulación dentro del contenedor HTML
            const render = Render.create({
                element: document.getElementById('tiroParabolicoContainer'),  // Contenedor HTML donde se mostrará la simulación
                engine: engine,
                options: {
                    width: 800,
                    height: 600,
                    wireframes: false  // Mostrar los cuerpos con relleno de color
                }
            });

            // Crear el suelo estático para la simulación
            const suelo = Bodies.rectangle(400, 580, 810, 40, { 
                isStatic: true,
                render: { fillStyle: '#2ecc71' }  // Color verde para el suelo
            });

            // Crear el proyectil que será lanzado
            const proyectil = Bodies.circle(100, 500, 20, { 
                restitution: 0.8,  // Rebote medio para el proyectil
                render: { fillStyle: '#e74c3c' }  // Color rojo para el proyectil
            });

            // Añadir el suelo y el proyectil al mundo físico
            World.add(engine.world, [suelo, proyectil]);

            // Obtener valores de velocidad y ángulo desde los controles
            const velocidad = document.getElementById('velocidad').value;
            const angulo = document.getElementById('angulo').value;

            // Convertir el ángulo a radianes
            const anguloRad = angulo * (Math.PI / 180);

            // Calcular las componentes de velocidad en los ejes x e y
            const velocidadX = velocidad * Math.cos(anguloRad);
            const velocidadY = -velocidad * Math.sin(anguloRad);

            // Aplicar la velocidad inicial al proyectil
            Body.setVelocity(proyectil, { x: velocidadX, y: velocidadY });

            // Iniciar el motor físico y el render para visualizar la simulación
            Engine.run(engine);
            Render.run(render);
        }
```



### 8. Simulación de Movimiento de Proyectiles

**HTML**

```html
    <div class="controls">
        <label for="velocidad1">Velocidad Proyectil 1:</label>
        <input type="range" id="velocidad1" min="5" max="20" value="10">
        
        <label for="velocidad2">Velocidad Proyectil 2:</label>
        <input type="range" id="velocidad2" min="5" max="20" value="12">
        
        <label for="velocidad3">Velocidad Proyectil 3:</label>
        <input type="range" id="velocidad3" min="5" max="20" value="14">
        
        <button onclick="simulacionProyectiles()">Iniciar Simulación de Proyectiles</button>
    </div>

    <div id="proyectilesContainer"></div>
```

**CSS**

```css
    <style>
        #proyectilesContainer {
            width: 800px;
            height: 600px;
            border: 1px solid #ccc;
        }

        .controls {
            margin-bottom: 10px;
        }
    </style>
```

**JavaScript**

```javascript
        function simulacionProyectiles() {
            // Crear los módulos necesarios de Matter.js
            const Engine = Matter.Engine,
                  Render = Matter.Render,
                  World = Matter.World,
                  Bodies = Matter.Bodies,
                  Body = Matter.Body;

            // Crear el motor físico
            const engine = Engine.create();

            // Crear el render para visualizar la simulación dentro del contenedor HTML
            const render = Render.create({
                element: document.getElementById('proyectilesContainer'),  // Contenedor HTML donde se mostrará la simulación
                engine: engine,
                options: {
                    width: 800,
                    height: 600,
                    wireframes: false  // Mostrar los cuerpos con relleno de color
                }
            });

            // Crear el suelo estático para la simulación
            const suelo = Bodies.rectangle(400, 580, 810, 40, { 
                isStatic: true,
                render: { fillStyle: '#2ecc71' }  // Color verde para el suelo
            });

            // Crear proyectiles con diferentes colores
            const proyectil1 = Bodies.circle(100, 300, 20, { 
                restitution: 0.8,  // Rebote moderado
                render: { fillStyle: '#e74c3c' }  // Color rojo para el proyectil 1
            });
            const proyectil2 = Bodies.circle(200, 300, 20, { 
                restitution: 0.8,  // Rebote moderado
                render: { fillStyle: '#3498db' }  // Color azul para el proyectil 2
            });
            const proyectil3 = Bodies.circle(300, 300, 20, { 
                restitution: 0.8,  // Rebote moderado
                render: { fillStyle: '#f1c40f' }  // Color amarillo para el proyectil 3
            });

            // Añadir el suelo y los proyectiles al mundo físico
            World.add(engine.world, [suelo, proyectil1, proyectil2, proyectil3]);

            // Obtener los valores de velocidad inicial desde los controles
            const velocidad1 = document.getElementById('velocidad1').value;
            const velocidad2 = document.getElementById('velocidad2').value;
            const velocidad3 = document.getElementById('velocidad3').value;

            // Aplicar las velocidades iniciales a los proyectiles
            Body.setVelocity(proyectil1, { x: parseFloat(velocidad1), y: -parseFloat(velocidad1) });
            Body.setVelocity(proyectil2, { x: parseFloat(velocidad2), y: -parseFloat(velocidad2) });
            Body.setVelocity(proyectil3, { x: parseFloat(velocidad3), y: -parseFloat(velocidad3) });

            // Iniciar el motor físico y el render para visualizar la simulación
            Engine.run(engine);
            Render.run(render);
        }
```



### 9. Simulación de Deslizamiento por Plano Inclinado

**HTML**

```html
    <div class="controls">
        <label for="angulo">Ángulo del plano:</label>
        <input type="range" id="angulo" min="0" max="45" value="30"> °

        <label for="friccion">Fricción de la caja:</label>
        <input type="range" id="friccion" min="0" max="1" step="0.1" value="0.1">
        
        <button onclick="simulacionPlanoInclinado()">Iniciar Simulación</button>
    </div>

    <div id="planoInclinadoContainer"></div>
```

**CSS**

```css
    <style>
        #planoInclinadoContainer {
            width: 800px;
            height: 600px;
            border: 1px solid #ccc;
        }

        .controls {
            margin-bottom: 10px;
        }
    </style>
```

**JavaScript**

```javascript
        function simulacionPlanoInclinado() {
            // Crear los módulos necesarios de Matter.js
            const Engine = Matter.Engine,
                  Render = Matter.Render,
                  World = Matter.World,
                  Bodies = Matter.Bodies,
                  Body = Matter.Body;

            // Crear el motor físico
            const engine = Engine.create();

            // Crear el render para visualizar la simulación dentro del contenedor HTML
            const render = Render.create({
                element: document.getElementById('planoInclinadoContainer'),  // Contenedor HTML donde se mostrará la simulación
                engine: engine,
                options: {
                    width: 800,
                    height: 600,
                    wireframes: false  // Mostrar los cuerpos con relleno de color
                }
            });

            // Obtener el ángulo y la fricción desde los controles
            const angulo = document.getElementById('angulo').value;
            const friccion = document.getElementById('friccion').value;

            // Convertir el ángulo de grados a radianes
            const anguloRadianes = angulo * (Math.PI / 180);

            // Crear el plano inclinado
            const planoInclinado = Bodies.rectangle(400, 400, 500, 20, { 
                isStatic: true,  // El plano no se mueve
                angle: anguloRadianes,  // Aplicar el ángulo del control
                render: { fillStyle: '#3498db' }  // Color azul para el plano
            });

            // Crear la caja con fricción ajustable
            const caja = Bodies.rectangle(200, 300, 40, 40, { 
                friction: friccion,  // Aplicar la fricción seleccionada
                restitution: 0.3,  // Añadir un pequeño rebote
                render: { fillStyle: '#e74c3c' }  // Color rojo para la caja
            });

            // Añadir el plano inclinado y la caja al mundo físico
            World.add(engine.world, [planoInclinado, caja]);

            // Iniciar el motor físico y el render para visualizar la simulación
            Engine.run(engine);
            Render.run(render);
        }
```



### 10. Simulación de Cañón

HTML

```html
    <div class="controls">
        <label for="velocidad">Velocidad del disparo:</label>
        <input type="range" id="velocidad" min="5" max="50" value="20">

        <label for="angulo">Ángulo del cañón:</label>
        <input type="range" id="angulo" min="0" max="90" value="45"> °
        
        <button onclick="simulacionCanon()">Disparar Cañón</button>
    </div>

    <div id="canonContainer"></div>
```

CSS

```css
    <style>
        #canonContainer {
            width: 800px;
            height: 600px;
            border: 1px solid #ccc;
        }

        .controls {
            margin-bottom: 10px;
        }
    </style>
```

JavaScript

```javascript
        function simulacionCanon() {
            // Crear los módulos necesarios de Matter.js
            const Engine = Matter.Engine,
                  Render = Matter.Render,
                  World = Matter.World,
                  Bodies = Matter.Bodies,
                  Body = Matter.Body;

            // Crear el motor físico
            const engine = Engine.create();

            // Crear el render para visualizar la simulación dentro del contenedor HTML
            const render = Render.create({
                element: document.getElementById('canonContainer'),  // Contenedor HTML donde se mostrará la simulación
                engine: engine,
                options: {
                    width: 800,
                    height: 600,
                    wireframes: false  // Mostrar los cuerpos con relleno de color
                }
            });

            // Crear el suelo estático para la simulación
            const suelo = Bodies.rectangle(400, 580, 810, 40, { 
                isStatic: true,
                render: { fillStyle: '#2ecc71' }  // Color verde para el suelo
            });

            // Crear la bala de cañón
            const bala = Bodies.circle(100, 500, 20, { 
                restitution: 0.8,  // Rebote moderado
                render: { fillStyle: '#e74c3c' }  // Color rojo para la bala
            });

            // Añadir el suelo y la bala al mundo físico
            World.add(engine.world, [suelo, bala]);

            // Obtener la velocidad y el ángulo desde los controles
            const velocidad = document.getElementById('velocidad').value;
            const angulo = document.getElementById('angulo').value;

            // Convertir el ángulo a radianes
            const anguloRad = angulo * (Math.PI / 180);

            // Calcular las componentes de velocidad en los ejes x e y
            const velocidadX = velocidad * Math.cos(anguloRad);
            const velocidadY = -velocidad * Math.sin(anguloRad);

            // Aplicar la velocidad inicial simulando el disparo de un cañón
            Body.setVelocity(bala, { x: velocidadX, y: velocidadY });

            // Iniciar el motor físico y el render para visualizar la simulación
            Engine.run(engine);
            Render.run(render);
        }

   

```





























