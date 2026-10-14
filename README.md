# MCSplat Interactive Demo

**MCSplat: Multi-View Photometric and Geometric Consistent Feed-Forward Gaussian Splatting for Driving Scenes**

[View the live demo](https://yfwang0824.github.io/yfwang-MCSplat/)

## Paper overview

The page presents the authors and affiliations, the abstract, and the method pipeline before the interactive demos. The original pipeline PDF is available alongside the web image under `assets/figures/`.

The visual design uses a light blue background, self-hosted Manrope typography, and responsive layouts. Manrope is distributed under the included SIL Open Font License in `assets/fonts/`. Demo assets begin loading as their sections approach the viewport.

## Interactive comparisons

- **Bilateral Grid Transformer:** synchronized ground-truth, BGT-on, and BGT-off image sequences for scenes 040, 050, and 199. Drag the divider, toggle correction, or seek through frames.
- **Gaussian reconstruction:** side-by-side UniSplat and MCSplat viewers for scenes 070 and 040. Drag to orbit, scroll to zoom, right-drag to pan, and press **F** inside a viewer to frame the scene.
- **Cross-lane novel-view synthesis:** comparison videos for scenes 018 and 027.

The Gaussian viewers load PLY files of approximately 39–55 MiB each. Initial loading time depends on the network connection and device.

## Run locally

From this folder, run:

```bash
python3 -m http.server 8765
```

Open [http://localhost:8765/](http://localhost:8765/). No build step is required.

## GitHub Pages

Publish the `main` branch from the repository root (`/`) in **Settings → Pages → Deploy from a branch**. The `.nojekyll` file lets GitHub Pages serve the static assets directly.

Use relative asset paths so the site works under `/yfwang-MCSplat/` as well as on a local server. Commit and push changes to `main` to update the published page.

## Viewer

The bundled viewer in `supersplat/` is based on [PlayCanvas SuperSplat Viewer](https://github.com/playcanvas/supersplat-viewer). Scene assets are stored in `assets/gaussians/`; the page configures the viewer through URL parameters.
