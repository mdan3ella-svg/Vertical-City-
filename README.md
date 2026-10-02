

## Files

- `index.html` — presentation, technical narrative and controls
- `style.css` — responsive layout and visual design
- `app.js` — bundled viewer, ready to run
- `assets/model.glb` — original 3D geometry
- `source/app-source.js` — readable, editable viewer source
- `source/package.json` — optional development build configuration
- `THREE-LICENSE.txt` — required Three.js MIT license notice

Keep the entire package together when hosting. The source folder is optional at runtime. There are no private hosting credentials or original hosting account settings in this export.

## View locally

Use an HTTP server rather than double-clicking `index.html`; browsers may block model loading from `file://`.

If Python is installed, open a terminal in this folder and run:

```sh
python -m http.server 8000
```

Visit `http://localhost:8000/`. Stop the server with Ctrl+C.

## Edit

Edit `index.html` to change text and `style.css` to change appearance. To change viewer behaviour, edit `source/app-source.js`, then run:

```sh
cd source
npm install
npm run build
```

Commit the rebuilt root `app.js`. Node.js is needed only for rebuilding, not for hosting or viewing.

## Viewer controls

- Drag to orbit; scroll or pinch to zoom; right-drag or two fingers to pan.
- Scene: select camera, projection, aspect ratio, FOV, lighting and display quality.
- Inspect: filter material groups, cut X/Y/Z sections, select/focus/isolate components, and measure two surface points.
- Measurements default to model units. Enter and confirm a calibrated scale only after checking a known dimension.
- Click the model canvas before using W/A/S/D to translate the camera and Q/E to move vertically. Shift increases movement speed. There is no collision detection.
- Present project starts the six-view guided narrative; Escape exits.
- Capture PNG exports the current model image with project credit.
- Design includes a review checklist and JSON export. Notes and check marks are session-only; export before closing or reloading.

## Model and engineering basis

125 source mesh objects; 137 rendered primitives; 76,792 triangles; 8 named materials plus default/unassigned material. Overall bounds are approximately 68.43 × 167.90 × 78.11 model units (X/Y/Z), including roads and below-grade geometry. Source Y extends from −32.60 to +135.30.

Presentation materials are a visual interpretation; Original materials restores the source appearance. Lighting is illustrative, not a photometric simulation. Section cuts are uncapped geometry views, not construction drawings. There is no structural analysis solver or code-compliance certification. Structural integrity, site conditions, real-world scale, loads, connections, reinforcement and foundation capacity require project-specific verification.

## Validation

The package preserves the checked model and compiled viewer. Model loading, geometry count, bounds, JavaScript compilation and asset references were verified. Browser visual testing was unavailable during creation. A modern browser with WebGL 2 is required.

## Credits

Design and concept: **Daniel Martins | Conceptsbydan | Vertascan**.
Rendering: Three.js, distributed under its included MIT license. This export does not assign a new license to the supplied architectural model or brand assets.
