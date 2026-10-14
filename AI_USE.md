# AI Use Statement

This project was built with substantial help from an AI coding assistant (Claude Code by Anthropic). This file records who did what, so readers can judge the work accurately.

## What the AI assistant did
- Wrote all of the application code (kept in the private source repository), working from a written brief, and later restructured it into a shared engine plus one module per topic.
- Drafted the licence text and set up the build tooling: Vite, Tailwind, ESLint, and the GitHub Pages workflow.
- Ran automated checks: lint, production build, a numerical test of the 3D net unfolding, a randomised test that each quadrilateral family keeps its rules while dragged, and a scripted headless-browser pass through all eight labs.
- Drafted the README, this statement, `RESEARCH.md` (research questions, study plan and ethics, from the author's stated goals) and `DECISIONS.md`. Decision-log entries the AI proposed are marked as AI proposals; entries marked "Author's reasoning: to be written" are deliberately left for the author.
- Set up the split between the private source repository and the public showcase repository, which holds the documents, screenshots and built demo.
- Drafted `CURRICULUM.md` (the topic list, grade placements and prerequisites) for the author to correct, and wrote up the author's reasoning in `DECISIONS.md` from the author's own statements.
- Built the visual proofs in the Circle Laws lab (`Watch why it's true`): angle at the centre, angle in a semicircle, angles in the same segment and the cyclic quadrilateral, plus a shared proof kit. This follows the author's direction that proofs must be watched, not read.
- Built the Foundations lab: seven Grade 6 stations (points and lines, angle as a turn, protractor, angle types, parallel and perpendicular lines, shape sorter, 3D shapes), including the everyday examples, which the author reviewed and approved.
- Drew the 127 everyday-object illustrations, as one set in a single line style, after the author chose in-house drawings over emoji (D-028).
- Built the Area & Perimeter lab (2D mensuration): six stations in which every formula is derived on screen, plus 12 more everyday illustrations. The trapezium area formula and the choice to derive rather than state formulas are the author's (D-001, D-027).
- Built the Quadrilateral Family lab: rule-keeping shapes, the property checklist, the family tree and the comparison table. The trapezium definition and the cone counting convention are the author's (D-026, D-027).
- Captured the screenshots in `docs/screenshots/` and added the copyright notice to the source files and the built bundle.
- Edited `STORY.md` from the author's own draft and account. The experiences, observations and arguments are the author's; the AI restructured the wording, added analytical terms, and flagged claims that needed qualifying.

## What the author did
- Wrote the product brief: the five labs and what each must show, the colour meanings, the target learners, the interaction rules (large drag targets, snap feedback, no hidden values), and the plain-language labels.
- Reviewed the result and made the project-level decisions: the name (Geometry Reader), the proprietary licence, the AI-disclosure policy, and the roadmap (English and visual interaction first; a Bangla version once the English version works as intended; audio not in current scope).
- Owns the educational rationale, which comes from experience as a student in Bangladesh and as a Grade 8 to O-Level mathematics teacher.

## Where the AI departed from the brief
The assistant changed or extended the brief in these places, and the author accepted the changes:
- The brief said walking round **any** shape always gives exactly 360° of turning. That only holds for shapes without a dent. The lab counts turns at dented corners as negative, and warns when edges cross, because then the rule no longer applies.
- The brief listed 3 of the "7 circle laws"; all 7 standard theorems were implemented.
- Curved solids are drawn with 32 flat facets so they can unfold. All displayed numbers use the exact formulas.

## Status of claims
The design aims (lower maths anxiety, lower sensory load, easier motor control) are **untested hypotheses**. No user study has been run yet.

## Commit provenance
Commits written by the assistant carry a `Co-Authored-By: Claude` trailer.
