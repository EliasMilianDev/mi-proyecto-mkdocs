---
title: Fundamentos HTML
---

# Fundamentos de HTML

HTML (HyperText Markup Language) es el lenguaje base de toda página web. Define la **estructura y el contenido**.

## Estructura básica

Todo documento HTML sigue esta estructura:

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8">
    <title>Mi página</title>
  </head>
  <body>
    <h1>Hola mundo</h1>
    <p>Este es mi primer párrafo.</p>
  </body>
</html>
```

## Etiquetas más usadas

| Etiqueta | Uso |
|----------|-----|
| `<h1>` – `<h6>` | Encabezados (de mayor a menor importancia) |
| `<p>` | Párrafo de texto |
| `<a href="">` | Enlace / hipervínculo |
| `<img src="">` | Imagen |
| `<ul>` / `<ol>` | Lista desordenada / ordenada |
| `<div>` | Contenedor genérico de bloque |
| `<span>` | Contenedor genérico en línea |
| `<form>` | Formulario |
| `<input>` | Campo de entrada |

## Ejemplo: Formulario de contacto

=== "HTML"
    ```html
    <form action="/enviar" method="POST">
      <label for="nombre">Nombre:</label>
      <input type="text" id="nombre" name="nombre" required>

      <label for="email">Correo:</label>
      <input type="email" id="email" name="email" required>

      <button type="submit">Enviar</button>
    </form>
    ```

=== "Resultado visual"
    ```
    [ Nombre: _________________ ]
    [ Correo: _________________ ]
    [       Enviar       ]
    ```

!!! warning "Validación HTML"
    Siempre valida tu HTML en [validator.w3.org](https://validator.w3.org) antes de publicar. Un HTML mal formado puede romper el diseño en algunos navegadores.

## Semántica HTML5

HTML5 introdujo etiquetas semánticas que describen el significado del contenido:

```html
<header>   <!-- Cabecera del sitio -->
<nav>      <!-- Barra de navegación -->
<main>     <!-- Contenido principal -->
<article>  <!-- Artículo independiente -->
<section>  <!-- Sección temática -->
<footer>   <!-- Pie de página -->
```

!!! note "¿Por qué usar etiquetas semánticas?"
    Mejoran la accesibilidad, el SEO y hacen el código más fácil de leer y mantener.

## Siguiente paso

Una vez que domines la estructura HTML, aprende a darle estilo con [CSS](css.md).
