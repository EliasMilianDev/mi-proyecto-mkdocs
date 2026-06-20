---
title: JavaScript
---

# JavaScript

JavaScript (JS) es el lenguaje de programación del navegador. Permite agregar interactividad y lógica a tus páginas [HTML](html.md).

## Variables y tipos de datos

=== "JavaScript moderno (ES6+)"
    ```js
    const nombre = "Ana";      // no reasignable
    let edad = 25;             // reasignable
    const activo = true;
    const precios = [10, 20, 30];
    ```

=== "JavaScript clásico (ES5)"
    ```js
    var nombre = "Ana";
    var edad = 25;
    var activo = true;
    var precios = [10, 20, 30];
    ```

!!! warning "Evita `var`"
    Usa `const` por defecto y `let` cuando necesites reasignar. `var` tiene comportamiento de hoisting que puede causar bugs difíciles de detectar.

## Funciones

=== "Declaración"
    ```js
    function saludar(nombre) {
      return `Hola, ${nombre}!`;
    }

    console.log(saludar("Ana")); // Hola, Ana!
    ```

=== "Arrow function"
    ```js
    const saludar = (nombre) => `Hola, ${nombre}!`;

    console.log(saludar("Ana")); // Hola, Ana!
    ```

## Manipulación del DOM

El DOM (Document Object Model) permite acceder y modificar elementos HTML desde JS.

```js
// Seleccionar elementos
const titulo = document.querySelector("h1");
const botones = document.querySelectorAll(".btn");

// Modificar contenido
titulo.textContent = "Nuevo título";
titulo.style.color = "blue";

// Crear y agregar elementos
const parrafo = document.createElement("p");
parrafo.textContent = "Este párrafo fue creado con JS";
document.body.appendChild(parrafo);
```

## Eventos

| Evento | Descripción |
|--------|-------------|
| `click` | Clic del mouse |
| `input` | Cambio en un campo de texto |
| `submit` | Envío de formulario |
| `keydown` | Tecla presionada |
| `load` | Página completamente cargada |
| `DOMContentLoaded` | HTML cargado (sin imágenes) |

```js
const boton = document.querySelector("#mi-boton");

boton.addEventListener("click", () => {
  alert("¡Botón presionado!");
});
```

## Fetch — llamadas a APIs

=== "Con async/await"
    ```js
    async function obtenerUsuario(id) {
      const respuesta = await fetch(`/api/usuarios/${id}`);
      const datos = await respuesta.json();
      return datos;
    }
    ```

=== "Con .then()"
    ```js
    fetch("/api/usuarios/1")
      .then(res => res.json())
      .then(datos => console.log(datos))
      .catch(err => console.error(err));
    ```

!!! note "Async/await vs Promises"
    Ambas formas son equivalentes. `async/await` es más legible para lógica secuencial; `.then()` es útil para encadenar múltiples operaciones en paralelo con `Promise.all()`.

??? info "¿Qué sigue después de JS básico?"
    Una vez que dominas estos fundamentos puedes explorar:

    - **Frameworks**: React, Vue, Angular
    - **Node.js**: JS en el servidor
    - **TypeScript**: JS con tipos estáticos
    - **Testing**: Jest, Vitest

## Regresa al inicio

Vuelve a la [página principal](index.md) para ver el resumen completo de la guía.
