# Portfolio Personal - Jhon Mendoza

Sitio web de currículum vitae y portfolio personal desarrollado con Astro, diseñado para presentar de forma profesional y atractiva mi perfil, experiencia, educación y habilidades.

## Características

- **Diseño Moderno y Responsivo**: Interfaz limpia y profesional que se adapta a todos los dispositivos
- **Navegación Suave**: Scroll suave entre secciones con navbar fijo
- **Secciones Completas**:
  - Hero con presentación personal
  - Sobre mí
  - Experiencia profesional
  - Educación y formación
  - Contacto
  - Footer
- **Optimización de Rendimiento**: Carga rápida gracias a Astro
- **SEO Optimizado**: Metadata configurada para mejor posicionamiento

##  Estructura del Proyecto

```text
/
 public/              # Archivos estáticos
 src/
    assets/          # Imágenes y recursos
    components/      # Componentes Astro
       Navbar.astro
       Hero.astro
       About.astro
       Experience.astro
       Education.astro
       Contact.astro
       Footer.astro
    layouts/         # Layouts base
       Layout.astro
    pages/           # Páginas del sitio
       index.astro
    styles/          # Estilos globales
 designInspo/         # Referencias de diseño
 package.json
```

## Tecnologías

- **[Astro](https://astro.build)** - Framework web moderno
- **HTML/CSS** - Maquetación y estilos

## Requisitos Previos

- Node.js (versión 18 o superior)
- npm o pnpm

## Instalación y Uso

### Instalar dependencias

```sh
npm install
```

### Iniciar servidor de desarrollo

```sh
npm run dev
```

El sitio estará disponible en `http://localhost:4321`

### Compilar para producción

```sh
npm run build
```

Los archivos compilados se generarán en la carpeta `./dist/`

### Previsualizar build de producción

```sh
npm run preview
```

## Comandos Disponibles

| Comando                   | Acción                                                |
| :------------------------ | :---------------------------------------------------- |
| `npm install`             | Instala las dependencias                              |
| `npm run dev`             | Inicia servidor de desarrollo en `localhost:4321`     |
| `npm run build`           | Genera el sitio para producción en `./dist/`          |
| `npm run preview`         | Previsualiza el build localmente antes de desplegar   |
| `npm run astro ...`       | Ejecuta comandos CLI de Astro                         |
| `npm run astro -- --help` | Muestra ayuda de la CLI de Astro                      |

## Despliegue

Este proyecto puede ser desplegado en múltiples plataformas:

- **[Vercel](https://vercel.com)** - Despliegue automático desde Git
- **[Netlify](https://netlify.com)** - Conexión directa con repositorio
- **[GitHub Pages](https://pages.github.com)** - Hosting gratuito
- **[Cloudflare Pages](https://pages.cloudflare.com)** - Red global CDN

Para más información sobre despliegue, consulta la [documentación de Astro](https://docs.astro.build/en/guides/deploy/).

## Licencia

Este proyecto es de uso personal.

## Contacto

Desarrollado por Jhon Mendoza

---

Si te gusta este proyecto, ¡no dudes en darle una estrella!
