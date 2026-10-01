# 🥾 Ejercicio de recopilación de HTML: «Sendeiros do Norte»

Tienes delante la web de un club de senderismo hecha **solo con HTML**.
El problema: está **llena de errores** y, además, **no se ve como debería**.

## 🎯 Tu misión

1. **Corregir todos los errores** de código que encuentres en `index.html`.
2. **Dejar la página exactamente como en las capturas** de más abajo.
3. **Entregar tu trabajo con un Pull Request** (te explicamos cómo al final).

> 💡 Hay errores de dos tipos: los que **rompen** la página (etiquetas sin cerrar, enlaces rotos, imágenes
> que no cargan...) y los que hacen que **no se vea igual** que la captura (una lista que no es una lista,
> una tabla sin bordes...). Y ojo: algunos errores **tapan a otros**. Cuando arregles uno, pueden aparecer más.

## 🚫 Reglas

- **Solo HTML. Nada de CSS.** No se permite `<style>`, ni `style="..."`, ni `<link rel="stylesheet">`.
- **Nada de etiquetas obsoletas o de formato**: `<center>`, `<font>`, `<b>`, `<i>`, `<u>`... Usa la etiqueta con el significado correcto.
- **Solo puedes modificar `index.html`.** No cambies nombres de archivos ni de carpetas, ni toques otros archivos.
- **Los textos ya están escritos.** No tienes que inventar contenido; tienes que arreglar y marcar bien lo que hay.
- Si una imagen o un enlace no funciona, el fallo está en el **HTML**, no en los archivos.

## 🖼️ Resultado esperado

Así tiene que verse tu `index.html` abierto en el navegador
(captura en 4 partes; [aquí tienes la captura completa](docs/resultado-completo.png)):

**1. Cabecera y presentación**

![Resultado esperado, parte 1: cabecera y presentación](docs/resultado-1-cabecera-y-presentacion.png)

**2. Rutas**

![Resultado esperado, parte 2: rutas](docs/resultado-2-rutas.png)

**3. Ranking, calendario y material**

![Resultado esperado, parte 3: ranking, calendario y material](docs/resultado-3-ranking-calendario-y-material.png)

**4. Vídeo, formulario y pie de página**

![Resultado esperado, parte 4: vídeo, formulario y pie](docs/resultado-4-video-formulario-y-pie.png)

## 📁 Estructura del proyecto

```
ejercicio-html-senderismo/
├── index.html              ← ¡El único archivo que debes editar!
├── rutas.html
├── aviso-legal.html
├── imagenes/
│   ├── logo.png
│   ├── portada.jpg
│   ├── pindo.jpg
│   ├── ezaro.jpg
│   ├── catasos.jpg
│   ├── cumbre-grande.jpg
│   └── poster.jpg
├── video/
│   └── presentacion.mp4
├── documentos/
│   └── guia-seguridad.pdf
├── docs/                   ← Capturas del resultado esperado
└── .github/                ← Comprobación automática (no lo toques)
```

## 🧰 Pistas

Si no recuerdas cómo se hace algo, aquí tienes una chuleta. Busca en la
[documentación de HTML de MDN](https://developer.mozilla.org/es/docs/Web/HTML) para ver ejemplos.

| Quiero... | Pista |
|-----------|-------|
| Imagen con pie de foto | `<figure>` y `<figcaption>` |
| Una cita | `<blockquote>` y `<cite>` |
| Lista que cuenta hacia atrás (3, 2, 1) | atributo `reversed` en `<ol>` |
| Numerar con letras (A, B, C) o con romanos (I, II, III) | atributo `type` en `<ol>` |
| Lista de términos y definiciones | `<dl>`, `<dt>`, `<dd>` |
| Celdas que ocupan varias columnas o filas | `colspan` y `rowspan` |
| Que la tabla tenga borde sin usar CSS | atributo `border` en `<table>` |
| Título, cuerpo y pie dentro de una tabla | `<caption>`, `<thead>`, `<tbody>`, `<tfoot>` |
| Subíndice y superíndice | `<sub>` y `<sup>` |
| Símbolos especiales (`&`, `©`, `€`, espacio que no se parte) | `&amp;` `&copy;` `&euro;` `&nbsp;` |
| Enlace que se abre en otra pestaña (de forma segura) | `target="_blank"` **y** `rel="noopener"` |
| Enlace que descarga un archivo | atributo `download` |
| Enlace a un correo / a un teléfono | `mailto:` / `tel:` |
| Enlace a otra parte de la misma página | `href="#id"` (el `id` tiene que existir y coincidir) |
| Vídeo | `<video>` con `controls`, `poster` y dentro `<source>` |
| Asociar un texto a su campo del formulario | `<label for="...">` + `id="..."` en el campo |
| Agrupar campos de un formulario | `<fieldset>` y `<legend>` |
| Que solo se pueda elegir una opción | botones `radio` con el **mismo** `name` |

## 🔎 Cómo comprobar tu trabajo

1. **Abre `index.html` en el navegador** (doble clic, o la extensión *Live Server* de VS Code)
   y compáralo con las capturas.
2. **Pasa el validador oficial del W3C**: <https://validator.w3.org/> (pestaña *Validate by File Upload*).
   Puede avisarte del atributo `border` de la tabla: es obsoleto, pero **en este ejercicio es obligatorio**
   porque no podemos usar CSS. Ignóralo.
3. **Ejecuta nuestro validador** (necesitas Python 3 instalado):

   ```bash
   python3 .github/scripts/validar.py index.html
   ```

   Te dirá la **línea** de cada error y qué requisitos de la página te faltan.
   Cuando subas tu Pull Request, GitHub lo ejecutará automáticamente y lo verás en la pestaña **Checks**.

> ⚠️ Que el validador diga «todo correcto» **no basta**: la página también tiene que **verse igual que la captura**.

## 📤 Cómo entregar tu trabajo (Pull Request)

1. **Haz un *fork*** de este repositorio (botón **Fork**, arriba a la derecha).
2. **Clona tu fork** en tu ordenador:

   ```bash
   git clone https://github.com/TU-USUARIO/ejercicio-html-senderismo.git
   cd ejercicio-html-senderismo
   ```

3. **Crea una rama** con tu nombre (apellidos primero, sin tildes ni espacios):

   ```bash
   git checkout -b ejercicio-apellido-nombre
   ```

4. **Edita `index.html`** y prueba los cambios en el navegador.
5. **Guarda tus cambios con commits.** Te recomendamos hacer varios commits pequeños
   (por ejemplo, uno por cada sección que arregles) en lugar de uno gigante:

   ```bash
   git add index.html
   git commit -m "Corrijo la cabecera y el menú"
   ```

6. **Sube tu rama** a tu fork:

   ```bash
   git push origin ejercicio-apellido-nombre
   ```

7. En GitHub, pulsa **Compare & pull request** y comprueba que la base es la **rama `main` del repositorio del profesor**.
   Pon este título y rellena la descripción:

   - **Título:** `Ejercicio HTML - Apellidos, Nombre`
   - **Descripción:** sigue la plantilla que te aparecerá.

## ✅ Lista de comprobación antes de entregar

- [ ] La página se ve igual que las capturas.
- [ ] No hay nada de CSS (`<style>`, `style=""`, `<link rel="stylesheet">`).
- [ ] No hay etiquetas obsoletas (`<center>`, `<font>`, `<b>`, `<i>`...).
- [ ] Todas las imágenes cargan y tienen su `alt`.
- [ ] Todos los enlaces funcionan (también los del menú y los de dentro de la página).
- [ ] Todas las etiquetas están bien cerradas y bien anidadas.
- [ ] El vídeo se ve y tiene controles.
- [ ] El formulario funciona: las etiquetas `<label>` están asociadas y solo se puede elegir un nivel.
- [ ] El validador de `.github/scripts/validar.py` no da ningún error.
- [ ] Solo he modificado `index.html`.
- [ ] Mi Pull Request tiene el título correcto.
