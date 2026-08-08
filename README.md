# Orbitals Studio

Interactive 3D hydrogenic orbitals and main-molecule electron fields.

**Live demo:** https://csasse123.github.io/OrbitalsStudio/

## What it is

- **Periodic table** H→Og — hydrogenic ψₙℓₘ with Slater Z_eff, n ≤ 20  
- **Main molecules** (~110) — multi-center density, MO ladder, nuclear correlation modes  
- **Science pack** — Morse / LJ potentials, spectroscopic constants, IE/EA/EN  

Everything runs **in your browser** (WebGL GPU). No server-side compute.

## Run locally

```bash
python3 -m http.server 8880
open http://localhost:8880/
```

Or open `index.html` / `molecule.html` after a local static server (ES modules need http, not `file://`).

## GPU

- WebGL2 via Three.js (`powerPreference: "high-performance"`)
- Analytic **volume ray-march** on the GPU (fragment shader)
- **GPU point cloud** for density seeds
- Adaptive quality tiers (steps / points / bloom) when frame time rises
- On-demand rendering (skip frames when idle)

## License

Personal / educational use. Built for demonstration and teaching.
