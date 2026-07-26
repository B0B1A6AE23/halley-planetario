[Español](README.md) · **English**

# HALLEY - night planetarium

**Live demo → [https://angeljgc-dev.github.io/halley-planetario/](https://angeljgc-dev.github.io/halley-planetario/)**

![Three.js](https://img.shields.io/badge/Three.js-WebGL-000000?logo=threedotjs&logoColor=white)
![GSAP](https://img.shields.io/badge/GSAP-ScrollTrigger%20%2B%20MotionPath-88CE02?logo=greensock&logoColor=black)
![ESM](https://img.shields.io/badge/ES%20Modules-importmap-F7DF1E?logo=javascript&logoColor=black)

Landing page for a night planetarium built on real WebGL: an endless starfield, a moon with a Fresnel glow and rings, and animated orbits. The astronomical show starts the moment you scroll.

| Hero | Section |
| --- | --- |
| ![Hero](docs/hero.png) | ![Section](docs/seccion.png) |

## Techniques

- **Three.js via importmap (ESM)** running next to global GSAP: a `THREE.Points` starfield with infinite z-recycling, a textured moon plus a Fresnel shader for the glow, and region-based fog.
- MotionPath for the orbits. One gotcha I left documented: `convertToPath` turns the `ellipse` into a `path`, so element-type CSS selectors stop matching it.
- ScrambleText on the astronomical figures, constellations drawn with `stroke-dasharray`, a magnetic button, and an eclipse transition done with transform only.
- Textures load with CORS open (Pexels images work straight as WebGL textures).

## Running locally

```bash
npx http-server . -p 8080
```

You need a server: ES modules and textures won't load over `file://`.

## License

Released under the [MIT](LICENSE) license. HALLEY is a made-up brand for portfolio purposes, not a real planetarium; any resemblance is coincidental. Third-party assets (photos, videos and 3D models) keep their authors' original licenses, see Credits.

## Credits

Photography and textures: [Pexels](https://www.pexels.com) · lunar texture from threejs.org.

---
Ángel Josué García Canteros · [github.com/angeljgc-dev](https://github.com/angeljgc-dev)
