# Vertascan NEXFORM — Deployment & Quality Assurance

This archive contains original four source apps in separate locations, a branded landing portal, four app-specific About/Features pages, and a review checklist. Host the extracted folder root on an HTTPS static site (GitHub Pages, Netlify, Cloudflare Pages). The portal links use relative paths, so they work with a GitHub repository subpath. Browser automation was attempted but navigation was blocked by the execution environment; browser runtime functionality is not verified.

## Software paths
- `/apps/scribeworks/index.html`
- `/apps/sequence/index.html`
- `/apps/sketchbim/index.html`
- `/apps/surreal/index.html`

The original app pages are preserved as supplied except for the specifically documented Surreal Interactive syntax patch. They have not been unified into a shared BIM object model. Do not claim certified IFC interchange, dependable code compliance, or commercial production readiness without real test evidence.

## Deployment steps
1. Extract the archive and upload its full contents to the repository's published branch/folder.
2. In GitHub: Settings → Pages → Deploy from branch → choose branch and `/ (root)` (or use a workflow).
3. Test `index.html`, each About/Features tab, and every application on actual hosted HTTPS URLs.
4. Test fresh project, edit, save, reload, recover, import, export and unsupported-file handling for every app.
5. Add a publicly published terms of service, privacy policy and support/contact channel *before* a production commercial launch; clarify storage and ownership.
6. Verify licenses of embedded Three.js, DRACO/Meshopt dependencies, fonts, third-party assets and any exported templates. Preserve required notices and attribution.
7. Establish versioning, release notes, issue management, regression suite, error telemetry (with consent/privacy controls), backups and rollback.

## Source scan summary (2026-10-22)
- SketchBIM: syntax clean across embedded executable scripts; runtime behavior NOT certified.
- SEQUENCE: syntax clean across embedded executable scripts; runtime behavior NOT certified.
- ScribeWorks: syntax clean across embedded executable scripts; runtime behavior NOT certified.
- Surreal Interactive: one pre-existing malformed JS block found in its supplied app source. In the packaged copy, the affected client-HTML export section was repaired and a specialty modeling block was isolated into its own script. Syntax now passes static checking; the actual export/import and specialty commands still require browser interaction testing.
- Surreal and SketchBIM carry large bundled JavaScript; neither has been split into module chunks or regression-tested under a browser automation suite.
- External online fonts/optional script URLs may require network. The bundle is not certified for 100% offline use.

## Release gate
- No uncaught JS errors in a clean browser console.
- Every visible UI action responds and changes state appropriately.
- Browser coverage: Chrome, Edge, Firefox, Safari, desktop and mobile breakpoints.
- No missing fonts/assets/optional scripts; graceful failure for unavailable network resources.
- Accessibility: keyboard navigation, focus, colour contrast, input labels, reduced-motion support where needed.
- Security: untrusted model/project parsing, XSS/exported HTML sanitization, payload size caps, Content Security Policy compatible with modules, no leaked user files.
- Data: schema/version migrations, autosave pressure testing, corrupt file handling, history, recovery, atomic exports.
- 3D: context loss recovery, GPU memory, WebGL compatibility, geometry integrity, import/export fidelity.
- AEC claims: verify dimension accuracy, units, coordinate transforms, classification data, schedules, code jurisdictions, and document outputs against expert test cases.
- Performance: load and memory benchmarks on mid-range laptop/tablet, e.g. large building/project documents.
- Copyright/trademark: search clearance for NEXFORM name and current app names before legal adoption or registration.
