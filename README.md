# VERTASCAN NEXFORM
## Design Intelligence Suite | Software Technical Overview

An integrated four-application architectural design platform for drafting, spatial planning, conceptual BIM and interactive visualization. This technical overview documents the delivered evaluation architecture, product roles, validation baseline and engineering requirements for a professional release.

**Document status:** Technical overview · Evaluation edition · 22 October 2026

> Product architecture and intended capabilities are distinguished from functions verified by testing. This is not a certification or independent code-compliance attestation.

## 01 — Executive overview

NEXFORM is Vertascan’s browser-based design intelligence suite, assembling four complementary architectural software environments under one product identity. It is conceived as a continuous practice-oriented workflow: precision drafting, spatial feasibility, conceptual BIM development and design visualization. The consolidated edition provides a common software launch point and separate product documentation while retaining each application as an independently accessible HTML application. It is an evaluation platform, not a claim of fully integrated commercial BIM interoperability.

## 02 — Platform architecture

The distribution uses a static web architecture: a responsive NEXFORM landing portal, application-specific information pages, and four dedicated application routes. Each tool preserves its own interface, state, commands and file workflows instead of sharing a runtime. This isolates application failures and allows iterative development and independent releases. Relative navigation paths support deployment beneath a GitHub Pages repository URL. Because a centralized project database, shared parametric schema, synchronized cross-app state and authenticated cloud service are not present in the current bundle, transitions between tools depend on the export/import capabilities of the particular applications, and must be verified format by format.

## 03 — ScribeWorks | Precision drafting

ScribeWorks addresses 2D vector production for architectural and related technical disciplines. The supplied interface exposes linework and modification tools, object/grid snapping, orthographic and polar tracking, layers, drawing styles, underlays, reusable architectural and MEP-oriented symbols, presentation presets and plotting-oriented outputs. Its scope is fast concept drafting, schematic documents and discipline coordination at drawing level. The presence of controls does not independently establish that every command and DXF/SVG export round-trips accurately; these remain part of the functional acceptance program.

## 04 — SEQUENCE | Spatial intelligence

SEQUENCE focuses on the early decisions that shape a building: space allocation, room relationships, form generation and development feasibility. Its interface includes spatial design workflows, analytical indicators, space lab functions and 2D/3D viewing concepts. It is positioned for iterative program studies, massing and preliminary architectural organization. Its data-driven outputs should be treated as decision support until geometry rules, calculation assumptions and relevant planning or building-code references have been separately validated.

## 05 — SketchBIM | Intelligent CAD and BIM

SketchBIM extends drafting toward object-oriented architectural modeling. Its supplied product is organized around building elements, geometric editing, levels and views, schedules, annotations and conceptual BIM information. It aims to coordinate design intent from linework through building elements and downstream documentation. This evaluation does not establish certified IFC exchange, standards-compliant quantities, jurisdiction-specific code approvals or production-ready construction documentation; those outcomes require documented conformance and reference-model testing.

## 06 — Surreal Interactive | Visualization and presentation

Surreal Interactive is the presentation layer: a browser-based environment for organizing imported assets, scene appearance, cameras, visual studies, animation concepts and client-facing project experiences. The supplied interface contains model/view controls, presentation/storyboard elements and export-oriented tools. Browser WebGL images must not be described as offline physically accurate path-traced renders. Complex FBX animation support, imported material fidelity and self-contained client HTML exports require targeted, asset-based verification. A malformed JavaScript block in the supplied version was corrected in the packaged evaluation build; runtime coverage of the affected functions is still outstanding.

## 07 — Design and interoperability principles

The four applications are distinct by design. The proposed long-term connective layer should use a versioned canonical project manifest with explicit units, local/global coordinate conventions, stable object identifiers, material references, asset provenance, transformation history and extension namespaces. Bidirectional conversion should state what survives each transfer, what is approximated and what is discarded. For dependable professional use, exchanges should preserve geometry, names, units, transforms and metadata through reference round-trip tests. Such a connective layer is a development direction, not a feature already implemented in this edition.

## 08 — Visualization and computational foundations

The tools combine conventional browser interfaces with 2D drawing and WebGL-based 3D workflows according to application. Engineering targets include deterministic command behavior, observable selection state, predictable camera manipulation, bounded import memory, context-loss handling, robust geometric validation and explicit fallbacks for unsupported assets or devices. Optional network dependencies and bundled libraries should be catalogued in a software bill of materials. No claim of fully offline operation or guaranteed compatibility across all GPUs is made without device testing.

## 09 — Quality assurance and verification model

NEXFORM adopts a layered verification strategy: (1) static source parsing and dependency checks; (2) functional interaction tests for every visible command and toggle; (3) model/data integrity checks including undo, redo, autosave, recovery and corrupt inputs; (4) import/export fixtures and file round-trips; (5) numerical accuracy checks for units, dimensions and AEC calculations; (6) rendering and input-device stress tests; and (7) accessibility, security and cross-browser testing. Every finding should record build ID, operating environment, reproducible steps, expected versus actual output, severity, ownership and retest evidence. This describes the release-quality framework; it does not assert the full matrix was executed.

## 10 — Observed evaluation baseline | 22 October 2026

Source-level checks reported clean embedded executable JavaScript parsing for ScribeWorks, SEQUENCE and SketchBIM. Surreal Interactive contained a malformed script section in the supplied source; the NEXFORM packaged version repaired the client HTML export section and separated an affected specialty block, after which static syntax checking passed. Browser-level automation was blocked in the previous evaluation environment. Accordingly, actual application runtime, user interactions, file persistence, interoperability and cross-device compatibility were not established. The suite is suitable for controlled evaluation, with defects to be recorded against each application and build.

## 11 — Security, privacy and licensing

A static Pages deployment publishes HTML, CSS, scripts and other served assets to visitors; it does not itself provide a confidential source-code boundary, multi-user access control, licensed execution, project encryption or durable server storage. Professional deployment requires threat modeling for untrusted project and model files, prevention of script injection in generated HTML, limits on imported assets, dependency updates, safe content handling, and a documented data-retention policy. Third-party licenses and model/texture/font rights must be checked, notices retained, and product naming cleared before commercial release.

## 12 — Commercial release criteria

A production candidate should pass repeatable browser test runs on target Chrome, Edge, Firefox and Safari versions; keyboard and touch interaction checks; accessibility review; load and memory budgets; project-file forward/backward compatibility tests; import/export fidelity baselines; predictable recovery from failed operations; cross-disciplinary calculation verification by qualified professionals where applicable; security review; legally reviewed product terms; and a documented release/rollback path. Unverified advanced BIM, code-checking and rendering functions must remain labeled as conceptual or experimental until qualified tests substantiate them.

## 13 — Product direction

The NEXFORM roadmap is a connected design lifecycle: author precise linework in ScribeWorks; organize program and feasibility in SEQUENCE; develop building information and geometry in SketchBIM; and communicate design intent through Surreal Interactive. The immediate priority is stabilization and clear per-app quality gates. The subsequent priority is a shared, versioned interchange contract—rather than collapsing four specialized engines into one fragile interface. Commercial maturity depends on measured reliability, traceable calculations and honest feature-level validation.

## Deployment reference

- Portal: `index.html`
- ScribeWorks: `apps/scribeworks/index.html`
- SEQUENCE: `apps/sequence/index.html`
- SketchBIM: `apps/sketchbim/index.html`
- Surreal Interactive: `apps/surreal/index.html`
- Upload the extracted site contents to the published repository root; enable GitHub Pages from the deployment branch.
- Evaluate on a live HTTPS URL and retain release evidence before inviting commercial users.

© 2026 Vertascan. Software concept and technical overview.
