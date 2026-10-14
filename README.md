# Geometry Reader

**See geometry move, instead of memorising it.** Geometry Reader is an interactive, browser-based geometry sandbox for students from Grade 6 to O-Level. Students drag points, lines and solids, and every angle, length, area and volume updates live, so theorems are discovered rather than recited.

**Live demo:** https://wasemafarzana1.github.io/geometry-reader-showcase/ (the app itself is in [`demo/`](demo/), as built and minified output) · **Status:** working prototype covering 35 of 65 planned geometry topics, not yet tested with students · **Author:** Wasema Farzana

![The 3D Spatial Matrix lab: a cylinder unfolding into its net, with live surface-area and scale readouts](docs/screenshots/05-spatial-matrix.png)

## Why it exists
In Bangladesh, the best tutoring and learning resources are concentrated among Dhaka's affluent, English-medium families. Students elsewhere, including in the author's home region of northern Bangladesh, fall behind for lack of access, and that gap is later called a gap in "merit". Geometry Reader aims to put a high-quality visual geometry resource within reach of any student with a browser. **[Read the full story →](STORY.md)**

## What it does
| Lab | Topic | What the student does |
|---|---|---|
| 1 · Foundations | The first ideas (Grade 6) | Seven stations: points, lines, rays and planes; an angle as a turn; using a protractor; types of angle; parallel and perpendicular lines; a shape sorter that names any shape you drag; and 3D shapes whose faces, edges and corners you count one by one. Every everyday example is drawn in-house, with the geometry in it highlighted. |
| 2 · Angle Runway | Angles on a line and at a point | Drags a ray and watches the two angles always sum to 180°, then expands it into a full 360° turn. |
| 3 · Vector Railways | Parallel lines and triangles | Tilts a line crossing two parallel rails and lights up the Z, F, C and X angle patterns; reshapes a triangle and sees the outside angle equal the two opposite inside ones. |
| 4 · Polygon Factory | Interior and exterior angles | Changes the number of sides from 3 to 10, splits the shape into triangles, and walks around its edge to watch the turns add up to 360°. |
| 5 · Quadrilateral Family | Squares, rectangles, rhombuses, parallelograms, trapeziums and kites | Picks a family's rules and stretches the shape, which keeps the rules however it is dragged; watches a rectangle become a square and the family tree light up; checks sides, angles, diagonals and symmetry live. |
| 6 · Circle Laws | All seven circle theorems | Slides points round a circle and watches each theorem hold, then watches four of them *proved* step by step. |
| 7 · Area & Perimeter | Perimeter, area, units, circles, arcs and sectors | Watches every formula being built on their own shape: edges unrolled onto a ruler, a parallelogram cut and slid into a rectangle, a trapezium and its spun copy making a parallelogram, a circle rolled out and sliced into a near-rectangle. |
| 8 · 3D Spatial Matrix | Solids, nets and scale | Unfolds four solids into flat nets and scales them up to see lengths grow ×k, areas ×k² and volumes ×k³. |

<table>
  <tr>
    <td><img src="docs/screenshots/02-vector-railways.png" alt="Vector Railways lab"></td>
    <td><img src="docs/screenshots/03-polygon-factory.png" alt="Polygon Factory lab"></td>
  </tr>
  <tr>
    <td><img src="docs/screenshots/04-circle-laws.png" alt="Circle Laws lab"></td>
    <td><img src="docs/screenshots/01-angle-runway.png" alt="Angle Runway lab"></td>
  </tr>
</table>

![Area & Perimeter lab: a trapezium and its spun copy make a parallelogram with base a + b, showing why the area is ½(a + b)h](docs/screenshots/09-area-perimeter.png)

![Quadrilateral Family lab: an isosceles trapezium with its bases, legs, equal diagonals and line of symmetry marked](docs/screenshots/08-quadrilateral-family.png)

![Foundations lab: using a protractor, with the correct scale lit up and the wrong-scale reading flagged](docs/screenshots/07-foundations.png)

**Visual proof:** the learner watches *why* the angle at the centre is double the angle at the edge. Two isosceles triangles fold onto themselves, and their equal corners slide into the centre.

![Visual proof of the angle-at-the-centre theorem, final step](docs/screenshots/06-visual-proof.png)

## Design principles
- **Topics first, curriculum second.** Each lab teaches the topic in depth, and matching it to O-Level, the national SSC/HSC syllabus or English Version is a separate layer.
- **Nothing hidden.** Every value is shown live as the student moves things.
- **Two kinds of language.** Every formal term sits beside a plain-language translation, e.g. *Supplementary Angles ➔ (180° Flat Runway Pairs)*.
- **Each colour has one job.** Indigo = something you can move, mint = proofs and truths, amber = measurements and warnings, cyan = vocabulary.
- **Built for every body and nervous system.** Large drag targets that snap to key values, full keyboard control, and a Calm mode that switches off flashes and motion.
- **Watch why, not just that.** Visual proofs animate the reason a theorem holds, on the learner's own figure.
- **Mathematically honest.** Where a simple rule has exceptions, the lab shows them, e.g. dented polygons.

The reasoning behind each choice is recorded in the **[decision log](DECISIONS.md)**.

## Roadmap
The goal is complete coverage of school geometry, from the idea of a point to O-Level and then college level. The **[curriculum map](CURRICULUM.md)** tracks every topic and its status.

1. **Now:** English version on the O-Level syllabus, refined with English-medium and English Version students.
   - **Visual proofs:** the learner *watches* why each theorem holds, as parts of the figure fold, swing and slide into place. Four are live: the angle at the centre, the angle in a semicircle, angles in the same segment, and the cyclic quadrilateral.
   - **Foundations lab: done.** Seven Grade 6 stations, each linked to everyday objects.
   - **Quadrilateral Family lab: done.** Rule-keeping shapes, a live family tree and a property table.
   - **Area & Perimeter lab: done.** Six stations; every formula, from l × w to πr² and ½(a + b)h, is derived on screen.
   - **Then:** the remaining topics in curriculum order (see the curriculum map), and visual proofs for the triangle and quadrilateral results.
2. **Next:** match every lab to the national SSC/HSC (NCTB) syllabus, and release a full Bangla version.
3. **Then:** college-level topics, and further "Readers" for other areas of mathematics.
4. **Throughout:** testing on low-cost phones, and classroom studies outside Dhaka. See the **[research agenda](RESEARCH.md)**.

## Documentation
| Document | For | Contents |
|---|---|---|
| [STORY.md](STORY.md) | Everyone | Why Geometry Reader exists |
| [CURRICULUM.md](CURRICULUM.md) | Educators, reviewers | Every planned topic, its grade, what it builds on, and its status |
| [DECISIONS.md](DECISIONS.md) | Reviewers, partners | Every major design decision, who made it, and why |
| [RESEARCH.md](RESEARCH.md) | Academics, funders | Research questions, hypotheses, study plan, ethics |
| [AI_USE.md](AI_USE.md) | Everyone | What the author did, and what the AI coding assistant did |
| [LICENSE](LICENSE) | Partners, buyers | Proprietary licence terms |

## How it is built
The author directs the design. An AI coding assistant writes the code from the author's briefs, under the author's review; see [AI_USE.md](AI_USE.md). Technically, it is a single-page React 18 app styled with Tailwind CSS, built as a shared engine (geometry maths, interaction, feedback and design system) with one module per topic, so new topics reuse the same foundations. All geometry and 3D rendering are hand-written SVG maths, with no 3D or physics libraries. It runs entirely in the browser: no server, no accounts, no data collection.

Checks performed so far: lint and production build on every push; a numerical test that the 3D nets unfold flat with surface area preserved; a numerical test that every quadrilateral family keeps its rules through thousands of random drags; a scripted browser walk-through of all eight labs; and a check that the layout works on a phone-width screen.

The source code is kept in a private repository. Authorised reviewers can be given access under a non-disclosure agreement; ask the author.

## About the author
**Wasema Farzana** is a mathematics educator teaching Grade 8 to O-Level students across English-medium and English Version curricula in Bangladesh. Geometry Reader is the first project in a planned series of visual mathematics tools, and part of the author's work at the intersection of HCI, education and AI & Society.

For collaboration, research or licensing enquiries, contact the author through [GitHub](https://github.com/wasemafarzana1).

## Licence
Copyright © 2026 Wasema Farzana. All rights reserved. This is **not** open-source software. No part of it may be used, copied, modified, distributed or sold without written permission. See [LICENSE](LICENSE).
