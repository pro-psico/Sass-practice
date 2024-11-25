
# Proyecto Platzi: Fundamentos de Sass

Este proyecto fue creado como parte del curso de **Fundamentos de Sass** en Platzi. El objetivo de este curso es aprender cómo mejorar la escritura de hojas de estilo utilizando Sass, un preprocesador que extiende las capacidades de CSS.

## Descripción

Este es un sitio web diseñado con Sass, utilizando varias características de este preprocesador, como variables, mixins, herencia y anidación. El sitio tiene un diseño responsivo, con un sistema de navegación y secciones interactivas que utilizan colores suaves y modernas prácticas de diseño web.

## Tecnologías utilizadas

- **Sass**: Preprocesador CSS que permite escribir código más limpio y organizado.
- **HTML5**: Estructura del sitio web.
- **CSS3**: Estilos visuales aplicados al sitio.
- **Flexbox**: Utilizado para la alineación y distribución flexible de elementos en el diseño.

## Características

### Variables
Las variables Sass permiten definir colores, fuentes y tamaños de texto de manera centralizada y reutilizable en todo el sitio:
```scss
$primary-color: #FFEFE7;
$secondary-color: #FFDAC6;
$tertiary-color: #BABD8D;
$primary-text-color: #7C6A0A;
$quaternary-color: #FA9500;
$font-stack: "IBM Plex Sans", sans-serif;
$paragraph-size: 1.5em;
```

### Mixins
Se usan mixins para encapsular reglas de estilo que pueden ser reutilizadas en varias partes del código:
```scss
@mixin flexCenter($direction, $content, $align){
    display: flex;
    flex-direction: $direction;
    justify-content: $content;
    align-items: $align;
}
```

### Anidación
La anidación de selectores es utilizada para mantener el código organizado y jerárquico:
```scss
nav {
    @include flexCenter(row, space-between, center);
    width: auto;
    padding: 15px;
    color: $primary-text-color;
    p {
        font-size: $paragraph-size;
        padding-left: 30px;
    }
}
```

### Herencia
Se utiliza la directiva `@extend` para compartir reglas de estilo entre clases, como en la sección de `furniture` que hereda de `healthcare`:
```scss
.furniture {
    @extend .healthcare;
    .product-card {
        color: white;
        background-color: $tertiary-color;
    }
}
```

## Estructura del Proyecto

El proyecto tiene la siguiente estructura:

```
/assets
    /scss
        styles.scss      # Archivo principal donde se importan todos los componentes
        _variables.scss  # Archivo con las variables globales
        _mixins.scss     # Archivo con los mixins utilizados
        _components.scss # Estilos para las diferentes secciones de la página (nav, article, etc.)
        _footer.scss     # Estilos para el pie de página
```

## Instalación

Para usar este proyecto, primero asegúrate de tener **Node.js** y **npm** instalados en tu máquina. Luego, sigue estos pasos:

1. Clona el repositorio:
   ```bash
   git clone https://github.com/tu-usuario/nombre-del-repositorio.git
   ```
2. Navega al directorio del proyecto:
   ```bash
   cd nombre-del-repositorio
   ```
3. Instala las dependencias:
   ```bash
   npm install
   ```
4. Compila los archivos Sass:
   ```bash
   npm run sass
   ```

Esto generará los archivos CSS a partir de los archivos Sass y podrás ver los cambios reflejados en tu proyecto.

## Contribuciones

Este proyecto es solo para fines educativos y fue desarrollado como parte de un curso. Si deseas contribuir, puedes realizar un fork del repositorio y enviar tus mejoras a través de pull requests.

## Licencia

Este proyecto es de código abierto bajo la licencia **MIT**.
