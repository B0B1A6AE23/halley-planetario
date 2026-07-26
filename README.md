[English](README.en.md) · **Español**

# HALLEY - planetario nocturno

**Ver en vivo → [https://angeljgc-dev.github.io/halley-planetario/](https://angeljgc-dev.github.io/halley-planetario/)**

![Three.js](https://img.shields.io/badge/Three.js-WebGL-000000?logo=threedotjs&logoColor=white)
![GSAP](https://img.shields.io/badge/GSAP-ScrollTrigger%20%2B%20MotionPath-88CE02?logo=greensock&logoColor=black)
![ESM](https://img.shields.io/badge/ES%20Modules-importmap-F7DF1E?logo=javascript&logoColor=black)

Landing de un planetario nocturno con WebGL real: campo de estrellas infinito, luna con glow Fresnel y anillos, y órbitas animadas. La función astronómica arranca en cuanto empiezas a deslizar.

| Hero | Sección |
| --- | --- |
| ![Hero](docs/hero.png) | ![Sección](docs/seccion.png) |

## Técnicas

- **Three.js por importmap (ESM)** conviviendo con GSAP global: starfield de `THREE.Points` con reciclado infinito en z, luna texturizada más un shader Fresnel para el glow, y niebla por regiones.
- MotionPath para las órbitas. Aquí hubo un gotcha que dejé documentado: `convertToPath` convierte el `ellipse` en `path`, y entonces el CSS que apuntaba al elemento por selector deja de aplicar.
- ScrambleText en las cifras astronómicas, constelaciones dibujadas con `stroke-dasharray`, botón magnético y una transición de eclipse hecha solo con transform.
- Las texturas van con CORS abierto (Pexels sirve directo como textura WebGL).

## Cómo correr

```bash
npx http-server . -p 8080
```

Necesita servidor: los módulos ES y las texturas no cargan bajo `file://`.

## Licencia

Código bajo licencia [MIT](LICENSE). HALLEY es una marca inventada para el portafolio, no un planetario real; si se parece a alguno es pura coincidencia. Lo de terceros (fotos, videos y modelos 3D) conserva su licencia original, ver Créditos.

## Créditos

Fotografía y texturas: [Pexels](https://www.pexels.com) · textura lunar de threejs.org.

---
Ángel Josué García Canteros · [github.com/angeljgc-dev](https://github.com/angeljgc-dev)
