# Directrices de Diseño - Sitio Web de Perfil Personal

## 📋 Índice
1. [Referencias Visuales](#referencias-visuales)
2. [Paleta de Colores](#paleta-de-colores)
3. [Tipografía](#tipografía)
4. [Layout y Composición](#layout-y-composición)
5. [Elementos Clave del Hero Section](#elementos-clave-del-hero-section)
6. [Espaciado y Grid](#espaciado-y-grid)
7. [Componentes UI](#componentes-ui)
8. [Responsive Design](#responsive-design)
9. [Interacciones y Animaciones](#interacciones-y-animaciones)

---

## 🎨 Referencias Visuales

### Hero Section - Referencias de Diseño

- Estilo minimalista y limpio
- Enfoque en tipografía bold
- Uso de espacios blancos generosos
- Diseño moderno con elementos visuales dinámicos
- Integración de imágenes/ilustraciones
- Balance entre texto e imagen
- Enfoque profesional y corporativo
- Jerarquía visual clara
- Elementos de CTA prominentes
- Uso de colores vibrantes
- Composición asimétrica
- Elementos decorativos sutiles
- Gradientes y efectos modernos

---

## 🎨 Paleta de Colores

### Paleta Principal
```css
/* Colores Primarios */
--primary-900: #0A0E27;      /* Azul oscuro profundo */
--primary-700: #1E293B;      /* Azul marino */
--primary-500: #3B82F6;      /* Azul brillante */
--primary-300: #60A5FA;      /* Azul claro */

/* Colores Secundarios */
--secondary-900: #1F2937;    /* Gris oscuro */
--secondary-700: #374151;    /* Gris medio */
--secondary-300: #D1D5DB;    /* Gris claro */
--secondary-100: #F3F4F6;    /* Gris muy claro */

/* Colores de Acento */
--accent-purple: #8B5CF6;    /* Púrpura */
--accent-teal: #14B8A6;      /* Teal */
--accent-orange: #F97316;    /* Naranja */
--accent-pink: #EC4899;      /* Rosa */

/* Neutrales */
--white: #FFFFFF;
--black: #000000;
--background: #FAFAFA;
--text-primary: #111827;
--text-secondary: #6B7280;
```

### Gradientes
```css
/* Gradientes Modernos */
--gradient-1: linear-gradient(135deg, #3B82F6 0%, #8B5CF6 100%);
--gradient-2: linear-gradient(135deg, #14B8A6 0%, #3B82F6 100%);
--gradient-3: linear-gradient(135deg, #F97316 0%, #EC4899 100%);
--gradient-hero: linear-gradient(180deg, rgba(0,0,0,0) 0%, rgba(0,0,0,0.05) 100%);
```

---

## ✍️ Tipografía

### Fuentes Recomendadas
```css
/* Títulos */
font-family: 'Inter', 'SF Pro Display', -apple-system, sans-serif;
font-weight: 700-900;

/* Cuerpo */
font-family: 'Inter', sans-serif;
font-weight: 400-500;
```

### Escala Tipográfica
```css
/* Headers */
--text-hero: clamp(3rem, 8vw, 6rem);        /* 48-96px */
--text-h1: clamp(2.5rem, 6vw, 4rem);        /* 40-64px */
--text-h2: clamp(2rem, 5vw, 3rem);          /* 32-48px */
--text-h3: clamp(1.5rem, 4vw, 2rem);        /* 24-32px */
--text-h4: clamp(1.25rem, 3vw, 1.5rem);     /* 20-24px */

/* Body */
--text-xl: 1.25rem;    /* 20px */
--text-lg: 1.125rem;   /* 18px */
--text-base: 1rem;     /* 16px */
--text-sm: 0.875rem;   /* 14px */
--text-xs: 0.75rem;    /* 12px */
```

### Pesos de Fuente
```css
--font-light: 300;
--font-normal: 400;
--font-medium: 500;
--font-semibold: 600;
--font-bold: 700;
--font-extrabold: 800;
--font-black: 900;
```

### Line Heights
```css
--leading-tight: 1.2;
--leading-snug: 1.375;
--leading-normal: 1.5;
--leading-relaxed: 1.625;
--leading-loose: 2;
```

---

## 📐 Layout y Composición

### Grid System
```css
/* Container Principal */
--container-max: 1280px;
--container-wide: 1536px;
--container-narrow: 960px;

/* Responsive Containers */
.container {
  max-width: var(--container-max);
  margin: 0 auto;
  padding: 0 clamp(1rem, 5vw, 3rem);
}
```

### Estructura del Hero Section

#### **Layout Asimétrico Moderno**
```
┌─────────────────────────────────┐
│ [NAV]                           │
│                                 │
│    [TÍTULO GRANDE]              │
│              [IMAGEN FLOTANTE]  │
│    [DESCRIPCIÓN]                │
│                                 │
│    [CTA]    [STATS/INFO]        │
└─────────────────────────────────┘
```

---

## 🎯 Elementos Clave del Hero Section

### 1. Título Principal
```css
.hero-title {
  font-size: var(--text-hero);
  font-weight: var(--font-black);
  line-height: var(--leading-tight);
  letter-spacing: -0.02em;
  color: var(--text-primary);
  margin-bottom: 1.5rem;
}
```

**Ejemplos de Copywriting:**
- `Hola, soy Jhon Mendoza` - Directo y personal
- `Desarrollador` - Profesional
- `Conectando negocio, tecnología y usuarios` - Creativo
- `Developer. Designer. Creator. Public Accountant` - Moderno

### 2. Subtítulo/Descripción
```css
.hero-subtitle {
  font-size: var(--text-xl);
  font-weight: var(--font-normal);
  line-height: var(--leading-relaxed);
  color: var(--text-secondary);
  max-width: 600px;
  margin-bottom: 2rem;
}
```

**Longitud recomendada:** 20-40 palabras  
**Propósito:** Describir especialización, valor único o propuesta

### 3. Call-to-Action (CTA)
```css
.cta-group {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
  align-items: center;
}

/* CTA Primary */
.btn-primary {
  padding: 1rem 2rem;
  font-size: var(--text-base);
  font-weight: var(--font-semibold);
  background: var(--primary-500);
  color: var(--white);
  border-radius: 0.5rem;
  transition: all 0.3s ease;
}

.btn-primary:hover {
  background: var(--primary-700);
  transform: translateY(-2px);
  box-shadow: 0 10px 25px rgba(59, 130, 246, 0.3);
}

/* CTA Secondary */
.btn-secondary {
  padding: 1rem 2rem;
  font-size: var(--text-base);
  font-weight: var(--font-semibold);
  background: transparent;
  color: var(--text-primary);
  border: 2px solid var(--secondary-300);
  border-radius: 0.5rem;
  transition: all 0.3s ease;
}
```

**Textos CTA recomendados:**
- Primary: "Ver Proyectos", "Contactar", "Ver Portafolio"
- Secondary: "Descargar CV", "Más sobre mí", "Ver Casos de Estudio"

### 4. Imagen/Visual
```css
.hero-image {
  width: 100%;
  max-width: 600px;
  border-radius: 1rem;
  object-fit: cover;
}

/* Estilo con sombra moderna */
.hero-image-wrapper {
  position: relative;
  filter: drop-shadow(0 25px 50px rgba(0, 0, 0, 0.15));
}

/* Blob decorativo detrás */
.hero-image-wrapper::before {
  content: '';
  position: absolute;
  width: 100%;
  height: 100%;
  background: var(--gradient-1);
  border-radius: 50%;
  filter: blur(60px);
  opacity: 0.3;
  z-index: -1;
}
```

### 5. Elementos Decorativos

#### **Badges/Tags**
```css
.hero-badge {
  display: inline-block;
  padding: 0.5rem 1rem;
  background: var(--secondary-100);
  color: var(--text-secondary);
  border-radius: 9999px;
  font-size: var(--text-sm);
  font-weight: var(--font-medium);
  margin-bottom: 1rem;
}
```

#### **Stats/Números**
```html
<div class="hero-stats">
  <div class="stat-item">
    <span class="stat-number">5+</span>
    <span class="stat-label">Años Experiencia</span>
  </div>
  <div class="stat-item">
    <span class="stat-number">50+</span>
    <span class="stat-label">Proyectos</span>
  </div>
  <div class="stat-item">
    <span class="stat-number">100%</span>
    <span class="stat-label">Satisfacción</span>
  </div>
</div>
```

#### **Social Links**
```css
.social-links {
  display: flex;
  gap: 1rem;
  margin-top: 2rem;
}

.social-link {
  width: 48px;
  height: 48px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  background: var(--secondary-100);
  transition: all 0.3s ease;
}

.social-link:hover {
  background: var(--primary-500);
  color: var(--white);
  transform: translateY(-4px);
}
```

---

## 📏 Espaciado y Grid

### Sistema de Espaciado
```css
/* Basado en múltiplos de 4px */
--space-1: 0.25rem;   /* 4px */
--space-2: 0.5rem;    /* 8px */
--space-3: 0.75rem;   /* 12px */
--space-4: 1rem;      /* 16px */
--space-5: 1.25rem;   /* 20px */
--space-6: 1.5rem;    /* 24px */
--space-8: 2rem;      /* 32px */
--space-10: 2.5rem;   /* 40px */
--space-12: 3rem;     /* 48px */
--space-16: 4rem;     /* 64px */
--space-20: 5rem;     /* 80px */
--space-24: 6rem;     /* 96px */
--space-32: 8rem;     /* 128px */
```

### Hero Section Spacing
```css
.hero-section {
  min-height: 100vh;
  padding: var(--space-20) 0;
  display: flex;
  align-items: center;
}

/* Gap entre elementos */
.hero-content > * + * {
  margin-top: var(--space-6);
}
```

---

## 🧩 Componentes UI

### Navegación
```css
.navbar {
  position: fixed;
  top: 0;
  width: 100%;
  padding: var(--space-6) 0;
  background: rgba(255, 255, 255, 0.8);
  backdrop-filter: blur(10px);
  z-index: 1000;
  border-bottom: 1px solid rgba(0, 0, 0, 0.05);
}

.nav-links {
  display: flex;
  gap: var(--space-8);
  align-items: center;
}

.nav-link {
  font-size: var(--text-base);
  font-weight: var(--font-medium);
  color: var(--text-primary);
  transition: color 0.3s ease;
  position: relative;
}

.nav-link:hover {
  color: var(--primary-500);
}

/* Underline animado */
.nav-link::after {
  content: '';
  position: absolute;
  bottom: -4px;
  left: 0;
  width: 0;
  height: 2px;
  background: var(--primary-500);
  transition: width 0.3s ease;
}

.nav-link:hover::after {
  width: 100%;
}
```

### Cards (para secciones después del Hero)
```css
.card {
  background: var(--white);
  border-radius: 1rem;
  padding: var(--space-8);
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
  transition: all 0.3s ease;
}

.card:hover {
  transform: translateY(-8px);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
}
```

### Botones - Estados Completos
```css
.btn {
  /* Base */
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
  padding: 1rem 2rem;
  font-size: var(--text-base);
  font-weight: var(--font-semibold);
  border-radius: 0.5rem;
  cursor: pointer;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  border: none;
  text-decoration: none;
  
  /* Hover */
  &:hover {
    transform: translateY(-2px);
  }
  
  /* Active */
  &:active {
    transform: translateY(0);
  }
  
  /* Focus */
  &:focus-visible {
    outline: 3px solid var(--primary-300);
    outline-offset: 2px;
  }
  
  /* Disabled */
  &:disabled {
    opacity: 0.5;
    cursor: not-allowed;
    transform: none;
  }
}
```

---

## 📱 Responsive Design

### Breakpoints
```css
/* Mobile First Approach */
--breakpoint-sm: 640px;    /* Móvil grande */
--breakpoint-md: 768px;    /* Tablet */
--breakpoint-lg: 1024px;   /* Laptop */
--breakpoint-xl: 1280px;   /* Desktop */
--breakpoint-2xl: 1536px;  /* Desktop grande */
```

### Hero Section Responsive
```css
.hero-section {
  /* Mobile: Stack vertical */
  display: flex;
  flex-direction: column;
  padding: var(--space-16) var(--space-4);
  min-height: 100vh;
}

@media (min-width: 768px) {
  .hero-section {
    /* Tablet: Más espaciado */
    padding: var(--space-20) var(--space-8);
  }
}

@media (min-width: 1024px) {
  .hero-section {
    /* Desktop: Layout de dos columnas */
    flex-direction: row;
    align-items: center;
    gap: var(--space-12);
    padding: var(--space-24) var(--space-12);
  }
  
  .hero-content {
    flex: 1;
  }
  
  .hero-visual {
    flex: 1;
  }
}
```

### Tipografía Responsive
```css
/* Títulos se escalan automáticamente con clamp() */
.hero-title {
  font-size: clamp(2.5rem, 8vw, 5rem);
}

.hero-subtitle {
  font-size: clamp(1rem, 3vw, 1.5rem);
}

/* Alineación responsive */
.hero-content {
  text-align: center;
}

@media (min-width: 1024px) {
  .hero-content {
    text-align: left;
  }
}
```

### CTAs Responsive
```css
.cta-group {
  flex-direction: column;
  width: 100%;
}

.cta-group .btn {
  width: 100%;
}

@media (min-width: 640px) {
  .cta-group {
    flex-direction: row;
    width: auto;
  }
  
  .cta-group .btn {
    width: auto;
  }
}
```

---

## ✨ Interacciones y Animaciones

### Animaciones de Entrada
```css
/* Fade In Up */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.hero-title {
  animation: fadeInUp 0.8s ease-out;
}

.hero-subtitle {
  animation: fadeInUp 0.8s ease-out 0.2s backwards;
}

.hero-cta {
  animation: fadeInUp 0.8s ease-out 0.4s backwards;
}

.hero-image {
  animation: fadeInUp 0.8s ease-out 0.6s backwards;
}
```

### Efectos de Hover
```css
/* Efecto de brillo */
.btn-primary {
  position: relative;
  overflow: hidden;
}

.btn-primary::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(
    90deg,
    transparent,
    rgba(255, 255, 255, 0.3),
    transparent
  );
  transition: left 0.5s ease;
}

.btn-primary:hover::before {
  left: 100%;
}
```

### Parallax Suave
```css
/* Para elementos decorativos */
.hero-background-shapes {
  position: absolute;
  transition: transform 0.1s ease-out;
}

/* JavaScript simple para parallax */
/*
document.addEventListener('mousemove', (e) => {
  const shapes = document.querySelectorAll('.hero-background-shapes');
  const x = e.clientX / window.innerWidth - 0.5;
  const y = e.clientY / window.innerHeight - 0.5;
  
  shapes.forEach((shape, i) => {
    const speed = (i + 1) * 20;
    shape.style.transform = `translate(${x * speed}px, ${y * speed}px)`;
  });
});
*/
```

### Scroll Reveal
```css
/* Elementos que aparecen al hacer scroll */
.scroll-reveal {
  opacity: 0;
  transform: translateY(50px);
  transition: all 0.8s ease-out;
}

.scroll-reveal.active {
  opacity: 1;
  transform: translateY(0);
}
```

### Typing Effect (Opcional para título)
```css
.typing-text {
  border-right: 3px solid var(--primary-500);
  animation: blink 0.7s step-end infinite;
}

@keyframes blink {
  0%, 100% { border-color: var(--primary-500); }
  50% { border-color: transparent; }
}
```

---

## 🎁 Extras y Mejores Prácticas

### Accesibilidad
```css
/* Focus visible para navegación por teclado */
*:focus-visible {
  outline: 3px solid var(--primary-500);
  outline-offset: 2px;
}

/* Contraste de colores mínimo 4.5:1 para texto normal */
/* Contraste de colores mínimo 3:1 para texto grande */

/* Prefers reduced motion */
@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}
```

### Performance
```css
/* Will-change para animaciones suaves */
.animated-element {
  will-change: transform, opacity;
}

/* Después de la animación */
.animated-element.animation-complete {
  will-change: auto;
}
```

### Optimización de Imágenes
- Usar WebP con fallback a PNG/JPG
- Lazy loading para imágenes below the fold
- Responsive images con `srcset`
- Comprimir imágenes (TinyPNG, Squoosh)

```html
<picture>
  <source 
    srcset="hero-image.webp" 
    type="image/webp"
  />
  <img 
    src="hero-image.jpg" 
    alt="Descripción"
    loading="lazy"
    width="600"
    height="600"
  />
</picture>
```

---

## 🚀 Checklist de Implementación

### Hero Section Esencial
- [ ] Título principal claro y grande
- [ ] Subtítulo descriptivo (20-40 palabras)
- [ ] Al menos 1 CTA principal
- [ ] Imagen o visual de calidad
- [ ] Navegación visible
- [ ] Responsive en móvil, tablet y desktop
- [ ] Animaciones de entrada suaves
- [ ] Enlaces a redes sociales

### Opcionales pero Recomendados
- [ ] Badge/tag con especialización
- [ ] Stats o números destacados
- [ ] CTA secundario
- [ ] Elementos decorativos (formas, gradientes)
- [ ] Efecto parallax sutil
- [ ] Dark mode
- [ ] Microinteracciones en hover

### Performance y Accesibilidad
- [ ] Imágenes optimizadas
- [ ] Alt text en todas las imágenes
- [ ] Contraste de colores adecuado
- [ ] Focus states visibles
- [ ] Prefers reduced motion
- [ ] Etiquetas semánticas HTML
- [ ] Meta tags para SEO

---

## 📝 Notas Finales

Este documento está diseñado para ser una guía completa pero flexible. Adapta estos elementos a tu estilo personal y a la narrativa que quieres contar. Recuerda:

1. **Menos es más**: No necesitas todos los elementos, elige los que mejor representen tu marca personal
2. **Consistencia**: Mantén un estilo visual coherente en todo el sitio
3. **Performance**: Optimiza imágenes y animaciones para tiempos de carga rápidos
4. **Accesibilidad**: Diseña pensando en todos los usuarios
5. **Mobile First**: Asegúrate de que se vea perfecto en móviles primero

---

*Documento creado el 18 de febrero de 2026*  
*Basado en 6 referencias visuales de hero sections*