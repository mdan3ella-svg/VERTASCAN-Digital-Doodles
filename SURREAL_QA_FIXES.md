# Surreal Interactive — Focused Reliability Patch

Part of **VERTASCAN Digital Doodles**.

## Corrections applied
- Viewport dimensions and device pixel ratio are clamped to prevent invalid camera aspect ratios in minimized or dynamically resized panes.
- Primitive creation now raises a descriptive error for unknown primitive types rather than attempting to call an undefined geometry factory.
- Project restoration rejects invalid payload structures before clearing the current scene. This is a basic structure check, not a comprehensive file security or schema validation system.
- Duplication clones the selected mesh's geometry and material(s), retaining non-primitive/imported custom meshes and their current parent, transform, visibility, and custom metadata; the duplicate gets a new object ID.
- Deletion respects the object lock flag and verifies that the object is in the editable scene array before modifying the array.
- Camera presets frame visible root scene objects rather than explicitly hidden root scene objects.

## Verification completed
- All 27 executable inline script blocks parse successfully using Node.js 22 `--check`.
- No duplicate HTML element IDs were detected.
- Packaged app and suite portal entrypoints remain at their original relative paths.

## Remaining limitations / release criteria
- Interactive Chromium smoke tests could not run in this environment because browser navigation to the local evaluation server and local file was blocked by administrator policy.
- User acceptance tests still required for 3D selection, transforms, path animation, camera presets, GLB/FBX/OBJ import, texture persistence, native saves, undo/redo, presentation HTML generation, PDF/JPG/MP4 workflows, and mobile layouts.
- This focused patch does **not** establish that every feature is defect-free or ready for commercial deployment. Realistic GLB/FBX export fidelity must be tested with representative assets.
