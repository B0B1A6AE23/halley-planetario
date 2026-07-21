[Español](README.md) · **English**

# HALLEY — Night Planetarium · Book Your Show

**Live demo → [https://b0b1a6ae23.github.io/halley-planetario/](https://b0b1a6ae23.github.io/halley-planetario/)**

![Three.js](https://img.shields.io/badge/Three.js-WebGL-000000?logo=threedotjs&logoColor=white)
![GSAP](https://img.shields.io/badge/GSAP-ScrollTrigger%20%2B%20MotionPath-88CE02?logo=greensock&logoColor=black)
![ESM](https://img.shields.io/badge/ES%20Modules-importmap-F7DF1E?logo=javascript&logoColor=black)

Landing page for a night planetarium built on **real WebGL**: an endless starfield,
a moon with a Fresnel glow and rings, and animated orbits — an astronomical show
that begins the moment you scroll.

| Hero | Section |
| --- | --- |
| ![Hero](docs/hero.png) | ![Section](docs/seccion.png) |

## Techniques

- **Three.js via importmap (ESM)** running alongside global GSAP: a `THREE.Points`
  starfield with infinite z-recycling, a textured moon plus a Fresnel shader for the
  glow, and region-based fog.
- **MotionPath** for the orbits (documented gotcha: `convertToPath` turns the
  `ellipse` into a `path`, so element-type CSS selectors stop matching).
- **ScrambleText** on the astronomical figures, constellations drawn with
  `stroke-dasharray`, a magnetic button, and an eclipse transition (transform only).
- CORS-open textures (Pexels images served straight as WebGL textures).

## Running locally

```bash
npx http-server . -p 8080
```

A server is required (ES modules and textures won't load over `file://`).

## License

Code released under the [MIT](LICENSE) license. **HALLEY** is a fictional brand
created to showcase portfolio work; any resemblance to a real business is purely
coincidental. Third-party assets (photographs, videos, and 3D models) retain their
authors' original licenses — see Credits.

## Credits

Photography and textures: [Pexels](https://www.pexels.com) · lunar texture from threejs.org.

---
**Ángel Josué García Cantero** · *cinematic landing pages series*.
