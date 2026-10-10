# Manual para principiantes: página de poemas

## 1. Qué vas a construir

Una página web de una sola pantalla larga con un título, una breve bienvenida y dos poemas. El archivo `poemas.html` contiene el contenido y el diseño. No necesitas instalar un programa especial para verla: ábrela con un navegador como Edge o Chrome.

## 2. Cómo abrirla

1. Busca el archivo `poemas.html` en la carpeta `outputs`.
2. Haz doble clic sobre él. Se abrirá en tu navegador.
3. Cuando hagas cambios, guarda el archivo y vuelve al navegador. Actualiza la página con `Ctrl + R` para verlos.

Para editar el código, puedes usar un editor de texto. Si usas el Bloc de notas, elige **Todos los archivos** al guardar para que el nombre termine en `.html` y no en `.txt`.

## 3. Las partes principales

### A. La estructura HTML

HTML organiza el contenido. Las etiquetas suelen tener apertura y cierre, por ejemplo `<h1>Mi título</h1>`. El texto queda entre ambas etiquetas.

- `<!doctype html>` indica que usamos HTML moderno.
- `<html lang="es">` contiene toda la página y señala que está en español.
- `<head>` guarda información de la página, como el título de la pestaña y los estilos.
- `<body>` contiene lo que las personas ven en pantalla.
- `<header>` es el encabezado.
- `<main>` agrupa el contenido central.
- `<article>` representa una sección independiente; aquí, cada poema.
- `<footer>` es el pie de página.
- `<h1>` es el título principal; `<h2>` es un título de menor nivel.
- `<p>` representa un párrafo.

Los comentarios como `<!-- ... -->` son notas para quien lee el código. No aparecen en la página.

### B. El diseño CSS

CSS cambia la apariencia. Está dentro de `<style> ... </style>` en la zona `<head>`.

Una regla se escribe así:

```css
body {
  color: #342b3b;
}
```

`body` selecciona la página completa. Dentro de las llaves están las propiedades. `color` cambia el color del texto y el valor hexadecimal `#342b3b` representa un color.

En esta página:

- `background` define el fondo.
- `font-family` elige la tipografía.
- `padding` crea espacio dentro de una sección.
- `margin` crea espacio fuera de una sección.
- `border-radius` redondea las esquinas.
- `.poema` selecciona todos los elementos que tienen `class="poema"`.
- `--acento` y las otras variables de `:root` guardan colores que se reutilizan. Puedes cambiar sus valores para cambiar la paleta.

### C. Cómo se conservan los versos

Cada poema usa un bloque como este:

```html
<div class="versos">Primera línea
Segunda línea
Tercera línea</div>
```

La clase `versos` está vinculada a esta regla CSS: `white-space: pre-line;`. Esa regla hace que los saltos de línea escritos en el poema se muestren como versos separados.

## 4. Cómo cambiar un poema

Busca el texto entre `<h2>` y `</h2>` y reemplázalo por el título que quieras. Luego reemplaza las líneas dentro de `<div class="versos">` y el nombre dentro del párrafo con clase `autor`.

Ejemplo:

```html
<article class="poema">
  <h2>Mi poema</h2>
  <div class="versos">Una línea tranquila,
otra para recordar.</div>
  <p class="autor">Tu nombre</p>
</article>
```

`<article>` abre una tarjeta y `</article>` la cierra. Mantén ambas etiquetas para que la tarjeta quede bien formada.

## 5. Cómo agregar otro poema

1. Selecciona desde `<article class="poema">` hasta su correspondiente `</article>`.
2. Copia y pega ese bloque debajo del último poema.
3. Cambia el título, los versos y el autor.
4. Guarda y actualiza el navegador.

## 6. Práctica recomendada

Haz un cambio a la vez y observa qué sucede:

1. Cambia el título principal.
2. Cambia un color en `:root`.
3. Escribe tu propio poema.
4. Agrega una tercera tarjeta.

Así podrás relacionar cada cambio del código con lo que ves en pantalla. Si algo deja de mostrarse bien, revisa que no falte una etiqueta de cierre como `</div>` o `</article>`.

## 7. Vocabulario

- **Etiqueta:** instrucción HTML entre signos `<` y `>`.
- **Atributo:** información adicional dentro de una etiqueta, como `class="poema"`.
- **Clase:** nombre que permite aplicar el mismo estilo a varios elementos.
- **Selector:** parte de CSS que indica a qué elemento se aplica una regla.
- **Navegador:** programa que muestra páginas web.
