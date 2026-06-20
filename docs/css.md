---
title: Estilos con CSS
---

# CSS — Hojas de Estilo en Cascada

CSS controla la presentación visual de los elementos [HTML](html.md). Separa el contenido del diseño.

## Formas de aplicar CSS

=== "Externo (recomendado)"
    ```html
    <link rel="stylesheet" href="estilos.css">
    ```

=== "Interno"
    ```html
    <style>
      body { background: #f0f0f0; }
    </style>
    ```

=== "Inline (evitar)"
    ```html
    <p style="color: red;">Texto rojo</p>
    ```

!!! tip "Buena práctica"
    Usa siempre un archivo CSS externo. Facilita el mantenimiento y permite compartir estilos entre páginas.

## Selectores básicos

| Selector | Ejemplo | Descripción |
|----------|---------|-------------|
| Elemento | `p { }` | Selecciona todos los `<p>` |
| Clase | `.card { }` | Selecciona elementos con `class="card"` |
| ID | `#menu { }` | Selecciona el elemento con `id="menu"` |
| Combinado | `nav a { }` | `<a>` dentro de `<nav>` |
| Pseudo-clase | `a:hover { }` | Enlace al pasar el mouse |

## El modelo de caja (Box Model)

Todo elemento HTML es una caja con estas capas:

```
┌─────────────────────────────┐
│          margin             │
│  ┌───────────────────────┐  │
│  │        border         │  │
│  │  ┌─────────────────┐  │  │
│  │  │     padding     │  │  │
│  │  │  ┌───────────┐  │  │  │
│  │  │  │  content  │  │  │  │
│  │  │  └───────────┘  │  │  │
│  │  └─────────────────┘  │  │
│  └───────────────────────┘  │
└─────────────────────────────┘
```

```css
.caja {
  width: 200px;
  padding: 16px;
  border: 2px solid #333;
  margin: 24px auto;
}
```

## Flexbox — diseño en una dimensión

```css
.contenedor {
  display: flex;
  justify-content: space-between; /* horizontal */
  align-items: center;            /* vertical */
  gap: 16px;
}
```

=== "Horizontal"
    ```css
    flex-direction: row; /* predeterminado */
    ```

=== "Vertical"
    ```css
    flex-direction: column;
    ```

!!! note "Flexbox vs Grid"
    **Flexbox** es ideal para layouts en una sola dirección (filas o columnas). Usa **CSS Grid** cuando necesites control en dos dimensiones a la vez.

## Diseño responsivo con Media Queries

```css
/* Móvil primero */
.tarjeta {
  width: 100%;
}

/* Tableta en adelante */
@media (min-width: 768px) {
  .tarjeta {
    width: 48%;
  }
}

/* Escritorio */
@media (min-width: 1024px) {
  .tarjeta {
    width: 30%;
  }
}
```

## Siguiente paso

Con HTML y CSS ya puedes crear páginas estáticas. Agrega interactividad con [JavaScript](javascript.md).
