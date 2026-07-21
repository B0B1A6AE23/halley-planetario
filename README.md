[English](README.en.md) · **Español**

# HALLEY — Planetario nocturno · Reserva tu función

**Ver en vivo → [https://b0b1a6ae23.github.io/halley-planetario/](https://b0b1a6ae23.github.io/halley-planetario/)**

![Three.js](https://img.shields.io/badge/Three.js-WebGL-000000?logo=threedotjs&logoColor=white)
![GSAP](https://img.shields.io/badge/GSAP-ScrollTrigger%20%2B%20MotionPath-88CE02?logo=greensock&logoColor=black)
![ESM](https://img.shields.io/badge/ES%20Modules-importmap-F7DF1E?logo=javascript&logoColor=black)

Landing de un planetario nocturno con **WebGL real**: campo de estrellas infinito,
luna con glow Fresnel y anillos, órbitas animadas — una función astronómica que
empieza al deslizar.

| Hero | Sección |
| --- | --- |
| ![Hero](docs/hero.png) | ![Sección](docs/seccion.png) |

## Técnicas

- **Three.js por importmap (ESM)** coexistiendo con GSAP global: starfield de
  `THREE.Points` con reciclado infinito en z, luna texturizada + shader Fresnel
  para el glow, niebla por regiones.
- **MotionPath** para órbitas (gotcha documentado: `convertToPath` convierte
  `ellipse`→`path` y el CSS por selector de elemento deja de aplicar).
- **ScrambleText** en cifras astronómicas, constelaciones dibujadas con
  `stroke-dasharray`, botón magnético, transición de eclipse (solo transform).
- Texturas con CORS abierto (Pexels sirve como textura WebGL).

## Cómo correr

```bash
npx http-server . -p 8080
```

Requiere servidor (los módulos ES y texturas no cargan bajo `file://`).

## Licencia

Código bajo licencia [MIT](LICENSE). **HALLEY** es una marca ficticia creada para demostrar trabajo de portafolio; cualquier parecido con un negocio real es coincidencia. Los recursos de terceros (fotografías, videos y modelos 3D) conservan la licencia original de sus autores — ver Créditos.

## Créditos

Fotografía y texturas: [Pexels](https://www.pexels.com) · textura lunar de threejs.org.

---
**Ángel Josué García Cantero** · Serie *páginas-película*.