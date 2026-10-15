# Decision Log

This log records the significant decisions behind Geometry Reader: what was decided, who made it, and why.

**Origin** says where each decision came from:
- **Author:** Wasema Farzana decided it.
- **AI proposal, accepted:** the AI coding assistant proposed it and the author approved it.

Sections marked *Author's reasoning: to be written* are left for the author to complete in the author's own words.

## How to add an entry

```markdown
## D-NNN · Short title
- **Date:** YYYY-MM-DD
- **Origin:** Author | AI proposal, accepted | AI proposal, rejected
- **Decision:** What was decided, in one or two sentences.
- **Alternatives considered:** What else was on the table.
- **Reasoning:** Why this option, in the author's words.
- **Consequences:** What this commits the project to, or rules out.
```

Rejected AI proposals belong here too. They show judgement as clearly as accepted ones.

---

## D-001 · Visual, manipulable geometry instead of text-first explanation
- **Date:** 2026-10-14
- **Origin:** Author
- **Decision:** Every concept is taught through direct manipulation: students drag points, lines and solids, and every angle, length, area and volume is shown live. No hidden values.
- **Alternatives considered:** Static diagrams with worked examples; video lessons.
- **Reasoning:** Grounded in the author's experience as a student in northern Bangladesh and as a teacher: text-only geometry resources blocked understanding, and visualisation unlocked it. See [STORY.md](STORY.md).
- **Consequences:** The product is interaction-heavy, so it needs a capable browser. Its effect on learning must be measured, not assumed.

## D-002 · Five labs spanning Grade 6 to O-Level
- **Date:** 2026-10-14
- **Origin:** Author
- **Decision:** The first release covers five labs: angles on a line and at a point; parallel lines and triangles; polygons; circle theorems; 3D solids, nets and scale factors.
- **Alternatives considered:** Building a smaller set of topics more deeply first.
- **Reasoning:** The goal is for every part of geometry to be covered. These five were a starting point, not a chosen boundary: "As I needed to start from somewhere, I started." (author)
- **Consequences:** The five labs are the first slice of a complete curriculum, not the whole product. The full scope is set by D-019 and mapped in [CURRICULUM.md](CURRICULUM.md).

## D-003 · Paired vocabulary: formal term beside a plain-language translation
- **Date:** 2026-10-14
- **Origin:** Author
- **Decision:** Every formal term appears with a plain-language version, e.g. *Supplementary Angles ➔ (180° Flat Runway Pairs)*, plus a real-world anchor for each lab.
- **Alternatives considered:** Formal terms only, with a separate glossary.
- **Reasoning:** Formal terms are where students freeze. Pairing each term with a plain-language translation removes the wall of jargon, but keeps the academic word that students must use in exams. In the author's words, the aim is to break complex concepts "down into articulate, realistic visualizations" and to reduce "excessive cognitive data load". The pairing should also reach into daily life: showing everyday objects with the shape or property in question, so that students recognise it the next time they see or handle one (see D-022).
- **Consequences:** Every label needs two versions. The Bangla release (D-011) needs a Bangla plain-language layer, not a literal translation.

## D-004 · Functional colour meaning, large touch targets, no diagnostic labels
- **Date:** 2026-10-14
- **Origin:** Author
- **Decision:** Each colour has one meaning: indigo = interactive, mint = proof or truth, amber = dimensions and warnings, cyan = vocabulary. Draggable targets are oversized and snap to key values. The interface never labels its users by diagnosis; it should simply feel right to those who need it.
- **Alternatives considered:** Decorative colour; standard-size controls; an explicit "accessibility mode" label.
- **Reasoning:** The product should help neurodivergent learners, and anyone with sensory or motor difficulties, without telling them that it is "for" them. Students should simply find that it works for them. A consistent colour meaning, large forgiving targets and the absence of labels all serve that aim.
- **Consequences:** Colour cannot be used decoratively anywhere in the product.

## D-005 · Implement all seven standard circle theorems
- **Date:** 2026-10-14
- **Origin:** AI proposal, accepted
- **Decision:** The brief named "7 circle laws" but specified three. All seven standard theorems were built.
- **Alternatives considered:** Build only the three specified.
- **Reasoning:** The title promised seven, and the syllabus examines all seven.
- **Consequences:** More content to maintain and to map to each syllabus.

## D-006 · Correct the brief's "always 360°" claim for exterior angles
- **Date:** 2026-10-14
- **Origin:** AI proposal, accepted
- **Decision:** The brief said walking round *any* polygon turns exactly 360°. That holds only for convex shapes. For dented (non-convex) shapes, turns at dented corners count as negative, and the lab warns when edges cross, because the rule then no longer applies.
- **Alternatives considered:** Build the claim exactly as written.
- **Reasoning:** A teaching tool must never teach a false general rule.
- **Consequences:** Establishes mathematical correctness as overriding the brief's wording.

## D-007 · Real fold-and-unfold nets; curved solids as 32 facets; exact formulas displayed
- **Date:** 2026-10-14
- **Origin:** AI proposal, accepted
- **Decision:** Nets unfold face by face about shared edges. Cylinders and cones are drawn with 32 flat facets so they can unroll. Every number on screen uses the exact formulas, not the facet approximation.
- **Alternatives considered:** Separate static net images; CSS-only 3D.
- **Reasoning:** A net that visibly unfolds from the solid shows *why* surface area is the sum of the faces.
- **Consequences:** The drawn curved surfaces are about 0.3% smaller than the true ones. The displayed values are exact.

## D-008 · Calm motion mode and full keyboard control
- **Date:** 2026-10-14
- **Origin:** AI proposal, accepted
- **Decision:** A "Motion: Calm" switch turns off flashes, pulses and auto-spin, and the app follows the device's reduce-motion setting. Every draggable point can also be moved with the arrow keys.
- **Alternatives considered:** Fixed animation; mouse and touch only.
- **Reasoning:** Fits D-004: the experience should adapt to sensory and motor needs without labelling anyone.
- **Consequences:** Every new interaction must support keyboard use and calm mode.

## D-009 · Disclose AI use openly
- **Date:** 2026-10-14
- **Origin:** AI proposal, accepted (the author initially preferred to hide AI involvement)
- **Decision:** AI involvement is stated in [AI_USE.md](AI_USE.md). AI-written commits carry a `Co-Authored-By` line. Private session links are excluded.
- **Alternatives considered:** Removing all trace of AI involvement.
- **Reasoning:** For an audience in HCI, AI & Society and education, and for investors doing due diligence, hidden AI use that is discovered later costs more trust than open disclosure. Disclosure also lets the author's own judgement be credited separately.
- **Consequences:** `AI_USE.md` must be kept up to date.

## D-010 · Proprietary licence, all rights reserved
- **Date:** 2026-10-14
- **Origin:** Author
- **Decision:** The project is not open source. Wasema Farzana holds copyright, and no use, copying, modification or sale is allowed without written permission.
- **Alternatives considered:** MIT (open source).
- **Reasoning:** The author intends Geometry Reader to become an edtech product and wants full intellectual, legal and creative control.
- **Consequences:** Contributors and partners will need written agreements. Copyright in AI-generated code may be limited (see [AI_USE.md](AI_USE.md)); protection rests mainly on the author's own creative and editorial contribution.

## D-011 · Phased rollout: English O-Level first, then the national curriculum and Bangla, then college
- **Date:** 2026-10-14
- **Origin:** Author
- **Decision:** Build and refine first in English on the O-Level syllabus, with English-medium and English Version students. Then map every lab to the national SSC/HSC (NCTB) syllabus and release a Bangla version for students in the periphery. Then extend to college level.
- **Alternatives considered:** Starting with the national curriculum in Bangla.
- **Reasoning:** The author teaches these students every day, so the design can be observed and refined closely before being extended to the students it was conceived for.
- **Consequences:** Until the Bangla release, the product mainly reaches the urban students the equity argument is about. [STORY.md](STORY.md) says so openly.

## D-012 · Topics first, curriculum second
- **Date:** 2026-10-14
- **Origin:** Author
- **Decision:** Every lab teaches its topic in depth, whatever the syllabus. Matching a lab to a particular syllabus is a separate layer on top.
- **Alternatives considered:** Building separate content for each syllabus.
- **Reasoning:** "Students regardless of curriculum must have the in-depth understanding of the topics." (author)
- **Consequences:** A syllabus-mapping table is needed before each new curriculum release.

## D-013 · Visual-first; audio out of current scope
- **Date:** 2026-10-14
- **Origin:** Author
- **Decision:** The current version focuses on visual interaction only. Audio narration may come later.
- **Reasoning:** "As they already have tutors, they need visual tools more than auditory tutors." (author) The students in the first phase (D-011) already have human explanation from teachers and tutors. What they lack is a way to *see* geometry move.
- **Open question:** This reasoning fits the first-phase students. Students in the periphery often have **no** tutor, so for the Bangla release (D-011) audio or written explanation may matter more. Revisit this decision before that release.
- **Consequences:** The product must not be described as offering audio support.

## D-014 · Name: Geometry Reader, the first of a series of "Readers"
- **Date:** 2026-10-14
- **Origin:** Author
- **Decision:** The product is called Geometry Reader. Later topics will follow the same pattern under their own "Reader" names.
- **Alternatives considered:** NeoGeometry; Geometry Spatial Engine.
- **Reasoning:** A "Reader" is where you can read everything about one topic, from complete novice to the most advanced level. (author)
- **Consequences:** The name commits each Reader to full coverage of its topic, from first ideas to advanced work (D-019). The code should keep each lab self-contained so that new topics can follow the same structure.

## D-015 · Design claims stay hypotheses until tested
- **Date:** 2026-10-14
- **Origin:** AI proposal, accepted
- **Decision:** Effects on maths anxiety, learning and accessibility are described as hypotheses until evaluated. See [RESEARCH.md](RESEARCH.md).
- **Reasoning:** Unsupported claims damage credibility with academic reviewers and investors alike.
- **Consequences:** Marketing language must stay within the evidence.

## D-016 · Privacy: no identifying places or people
- **Date:** 2026-10-14
- **Origin:** Author
- **Decision:** Public documents say "northern Bangladesh". They never name the author's district or any schools, neighbourhoods or tutoring families.
- **Reasoning:** The repository is public, and the families and students the author worked with deserve anonymity.
- **Consequences:** Applies to every document and commit.

## D-017 · Private source repository, public showcase repository
- **Date:** 2026-10-14
- **Origin:** AI proposal, accepted
- **Decision:** The source code stays in a private repository permanently. A separate public repository holds the documentation, the screenshots and the built demo.
- **Alternatives considered:** Making the source repository public under the proprietary licence.
- **Reasoning:** Copyright in AI-written code may be limited, while trade-secret protection depends only on keeping the code secret, and publishing it gives that up for good. The public showcase still gives reviewers, professors and investors everything they need. Source access is granted only under an NDA.
- **Consequences:** The showcase must be updated by hand after each change. The built demo is minified, but its JavaScript still reaches every visitor's browser; that is unavoidable for a web app.

## D-018 · Header tagline: "Visual Geometry Sandbox" instead of "Anti-Phobia Sandbox"
- **Date:** 2026-10-14
- **Origin:** AI proposal, accepted
- **Decision:** The app header describes what the product is, not an outcome it has not yet shown.
- **Reasoning:** "Anti-Phobia" claims an untested effect on anxiety (see D-015), and it is the first thing reviewers and investors see.
- **Consequences:** The aim of reducing maths anxiety remains in RESEARCH.md as hypothesis H2.

## D-019 · Goal: complete coverage of geometry, from first ideas to advanced work
- **Date:** 2026-10-14
- **Origin:** Author
- **Decision:** Geometry Reader will cover the whole of school geometry, from the first ideas (point, line, shape) to O-Level and then college level. It includes the topics missing from the first release: foundations, quadrilaterals, 2D mensuration, Pythagoras, congruence and similarity, transformations, constructions, trigonometry, coordinate geometry and vectors.
- **Reasoning:** Follows from D-002 and D-014: a Reader is meant to hold everything about its topic.
- **Consequences:** [CURRICULUM.md](CURRICULUM.md) tracks every topic, its grade, what it builds on, and its status.

## D-020 · Build order: Proof Mode first, then the missing foundations
- **Date:** 2026-10-14
- **Origin:** Author
- **Decision:** After restructuring the code (D-021), build in this order: (1) Proof Mode for the theorems already in the app; (2) a Foundations lab; (3) a Quadrilateral Family lab; (4) 2D mensuration with formulas derived on screen; (5) the remaining topics in curriculum order.
- **Alternatives considered:** Foundations first, following the order in which students learn.
- **Reasoning:** Proof Mode deepens the five labs that already exist, so it improves what reviewers can see today.
- **Consequences:** The labs move from *showing* that a theorem holds to *explaining why* it holds.

## D-021 · Restructure the code into a shared engine plus one module per topic
- **Date:** 2026-10-14
- **Origin:** AI proposal, accepted
- **Decision:** The single 3,300-line file is split into a shared engine (maths, interaction, feedback, design system), one file per lab, and separate content files (such as the glossary).
- **Reasoning:** Complete coverage (D-019) means dozens of topics. That is unmanageable in one file, and new topics should reuse the same engine.
- **Consequences:** Adding a topic means adding one lab file and registering it.

## D-022 · Everyday-object anchors for every shape and property
- **Date:** 2026-10-14
- **Origin:** Author
- **Decision:** Each shape and property is linked to everyday objects that students see and handle, shown visually where possible rather than as a single line of text.
- **Reasoning:** Students should relate to the idea and think of it the next time they see or work with the object. (author)
- **Consequences:** Each lab needs a set of everyday examples. The Bangla release should use examples from students' own surroundings.

## D-023 · Proofs are visual and curriculum-neutral, not exam-style write-ups
- **Date:** 2026-10-14
- **Origin:** Author
- **Decision:** Each proof is shown as an animation the learner watches step by step, with short plain-language captions. Pieces of the figure fold, swing and slide so that the reason becomes visible. Proofs do not follow any exam board's written format.
- **Alternatives considered:** O-Level-style statement-and-reason lines; both formats side by side.
- **Reasoning:** "The learner must not just wonder how did this happen, they must see and watch how it happened actually through visualisation." The aim is in-depth understanding of the topic, not a particular curriculum's style of answer (D-012). (author)
- **Consequences:** Every proof needs a visual mechanism, not just text. Proofs stay live, so if the learner drags the figure, the same argument replays on the new shape. The first proof built is the angle at the centre, chosen because three other circle theorems follow from it.

## D-024 · Lab badges describe the topic, not an exam
- **Date:** 2026-10-14
- **Origin:** AI proposal, accepted
- **Decision:** The Circle Laws badge changed from "A* Exam Engine" to "Circle Theorems".
- **Reasoning:** It is consistent with topics first (D-012) and with curriculum-neutral proofs (D-023). The product teaches the topic itself, not one exam's grade.
- **Consequences:** New labs are labelled by grade range and topic.

## D-025 · Foundations lab: seven stations for Grade 6
- **Date:** 2026-10-14
- **Origin:** AI proposal, built at the author's request; open points resolved by the author
- **Decision:** One lab, placed first in the navigation, with seven stations matching curriculum topics A1–A7. Each station pairs a hands-on figure with paired vocabulary (D-003) and an everyday-objects card (D-022).
- **Resolved by the author:**
  1. **Everyday examples:** approved as drafted, including the examples familiar in Bangladesh (a samosa, a carrom board, a paper kite or ghuri, the national flag).
  2. **Emoji or illustrations:** replaced by in-house illustrations (D-028).
  3. **The trapezium definition:** exactly one pair of parallel sides (D-027).
  4. **Lab names:** Lab 2 renamed from "Foundation Runway" to "Angle Runway", so it no longer sounds like Lab 1.
- **Consequences:** Topics A1–A7 are built (see [CURRICULUM.md](CURRICULUM.md)).

## D-026 · Counting faces, edges and vertices on curved solids
- **Date:** 2026-10-14
- **Origin:** AI proposal, confirmed and extended by the author
- **Decision:** Curved surfaces count as faces, listed separately from flat faces. Circular rims count as edges. Cylinder: 3 faces (2 flat, 1 curved), 2 edges, 0 vertices. Cone: 2 faces (1 flat, 1 curved), 1 edge, 1 vertex. Sphere: 1 curved surface, 0 edges, 0 vertices.
- **Author's addition:** Teach the disagreement openly. Strict definitions say a vertex is where straight edges meet, so a cone has 0 vertices and only 1 face (only flat surfaces count). Students should know why books differ, and should know the word everyone agrees on for the cone's tip: the **apex**.
- **Reasoning:** The standard school answer is the one students are marked on, but a learner who meets the other convention should understand it rather than think they were taught wrong. (author)
- **Consequences:** The 3D Shapes station shows a "Why do some books disagree?" card for curved solids, with the apex explained for the cone. Euler's pattern (F + V − E = 2) is kept to flat-faced solids.

## D-027 · A trapezium has exactly one pair of parallel sides
- **Date:** 2026-10-14
- **Origin:** Author
- **Decision:** A trapezium is a quadrilateral with exactly one pair of parallel sides. The parallel sides are the **bases**; the other two are the **legs**. Types: isosceles (equal legs), right (two right angles) and scalene. Area = ½(a + b)h, where a and b are the bases and h is the distance between them. "Trapezium" in the UK and Bangladesh is "trapezoid" in the USA.
- **Alternatives considered:** The inclusive definition (at least one pair), under which every parallelogram is also a trapezium.
- **Reasoning:** This is the definition the author's students are taught and examined on. (author)
- **Consequences:** In the family tree, Parallelogram does not sit under Trapezium. The lab says so, and notes that some books, especially in the USA, use the inclusive definition. Every other family is inclusive: a square is a rectangle, a rhombus, a parallelogram and a kite. The area formula will be derived on screen in the 2D Mensuration lab (D-001).

## D-028 · In-house line illustrations for everyday objects
- **Date:** 2026-10-14
- **Origin:** Author (no budget; design time given); drawings by the AI assistant
- **Decision:** Every everyday example is drawn as a small line illustration in one shared style. The geometric idea the object carries (a right angle, a parallel pair, an apex, a turn) is drawn in amber, so the eye goes straight to it. Emoji remain only as a fallback.
- **Alternatives considered:** Emoji, which look different on every device and cannot highlight the geometry; commissioned illustrations or photographs, for which there is no budget.
- **Reasoning:** Illustrations look the same on every phone, match the app's design, and point at the maths in the object rather than just naming it.
- **Consequences:** 144 drawings live in `src/content/illustrations.jsx` (115 at first, then 12 for Area & Perimeter and 17 for the labs in D-031). New examples need a new drawing. For the Bangla version, objects from students' own surroundings can be added in the same style.

## D-029 · Quadrilateral Family lab: keep the rules, change the shape
- **Date:** 2026-10-14
- **Origin:** AI proposal, built at the author's request; kite definition confirmed by the author
- **Decision:** The learner chooses a family's rules (for example "all four corners stay at 90°") and drags the corners. The shape keeps those rules however it is stretched, so the learner sees which properties always come with the rules and which belong to one drawing only. A family tree lights up every family the shape belongs to; tapping a box gives the shape that family's rules. A side-by-side table lists what each family always has, measured by the app on a typical example of each family rather than typed in.
- **Reasoning:** A fixed diagram shows one shape, so "every square is a rectangle" has to be taken on trust. Stretching a rectangle until it *becomes* a square, while it never stops obeying the rectangle rules, shows the family relationship happening (D-001). That this helps learners accept the inclusive families is a hypothesis to test (H4 in [RESEARCH.md](RESEARCH.md)). Measuring the table from real shapes means the text cannot contradict the figure.
- **Kite definition (author):** Every rhombus is a kite, but not every kite is a rhombus. A kite is a quadrilateral with two pairs of equal adjacent sides; a rhombus has all four sides equal, so it qualifies. The tree therefore joins Kite to Rhombus, and a square counts as a kite too. A kite's line of symmetry is the diagonal joining the corners where the equal sides meet. It is not always the longer diagonal.
- **Consequences:** Topics D1–D3 are built. The lab is placed after Polygon Factory, so Circle Laws and 3D Spatial Matrix become Labs 6 and 7. Visual proofs of the family properties (for example, why a parallelogram's opposite angles are equal) are still to come.

## D-030 · Area & Perimeter lab: every formula is watched being built
- **Date:** 2026-10-14
- **Origin:** AI proposal, built at the author's request ("go on with 2D mensuration"); open points listed for author review
- **Decision:** One lab with six stations (F1–F6). No formula is stated without first being built on the learner's own shape:
  - **Perimeter:** the outline is cut at the corners and laid flat along a ruler.
  - **Rectangle:** unit squares fill one row, then the rows stack: l × w.
  - **Parallelogram:** a triangle is cut off and slid across, making a rectangle: b × h.
  - **Triangle and trapezium:** an identical copy is spun 180°, making a parallelogram, so each shape is half of it: ½bh and ½(a + b)h (D-027).
  - **Units:** a square unit is filled with smaller squares, row by row, so the area factor is the length factor squared.
  - **Circle:** rolled one turn to show C = πd; then cut into slices and laid in a row that approaches a rectangle πr by r, so A = πr².
  - **Arc and sector:** shown as the fraction θ/360 of the whole circle.
  - **Compound shapes:** worked three ways, all giving the same area.
- **Reasoning:** D-001 (formulas derived, not stated) and D-023 (visual proofs). The chain rectangle → parallelogram → triangle → trapezium means each formula rests on the one before it.
- **Choices the AI made, for author review:**
  1. **Generic units.** Figures use "units" and "u²" rather than cm or m, so one figure works for any unit. The Units station uses real units.
  2. **Rounding.** Calculations use the exact value of π; answers are shown to 2 decimal places. Perimeters with slanted sides are shown to 1 decimal place.
  3. **Whole-number sizes.** Most shapes snap to whole units, so that squares can be counted. The circle radius moves in quarter units.
  4. **Local units.** The Units station mentions the decimal, a land unit used in Bangladesh (1 decimal = 1/100 acre, about 40.5 m²), as an everyday example only. Should the Bangla version teach local units (decimal, katha, bigha) properly?
  5. **Parallelogram lean.** The cut-and-slide proof needs the top to lean by no more than the base length, so the lab stops the lean there. A steeper parallelogram needs several cuts; that case is not shown yet.
- **Consequences:** Topics F1–F6 are built. The lab is placed before the 3D Spatial Matrix, which uses these formulas, so the 3D lab becomes Lab 8. The station layout is now a shared engine part (`StationLab`), used by Foundations and this lab.


## D-031 · Build every remaining O-Level topic
- **Date:** 2026-10-15
- **Origin:** Author ("build all of the next"); labs built by the AI assistant; choices below are for author review
- **Decision:** Every remaining topic in sections A–L of the curriculum map is now built, in eight new labs and one addition to an existing lab:
  - **Triangles:** classify; isosceles and equilateral; the triangle inequality; Pythagoras; congruence; similarity (C1, C4–C8).
  - **Circle Basics:** parts of a circle; chords (E1, E9).
  - **Volume & Spheres:** units of volume and capacity; sphere and hemisphere (G4, G5).
  - **Symmetry & Transformations:** symmetry; reflect, rotate, translate; enlargement; combine and undo; tessellation (H1–H4, D7).
  - **Constructions & Loci:** constructions; scale drawings and maps; loci (I1–I3).
  - **Coordinate Geometry:** plotting; distance, gradient and midpoint; y = mx + c; parallel and perpendicular (J1–J4).
  - **Trigonometry:** SOH CAH TOA; elevation and depression; bearings; sine and cosine rules; trigonometry in 3D (K1–K4, B5).
  - **Vectors:** basics; proofs with vectors (L1, L2).
  - **Additions:** a "Why 360°?" proof in the Quadrilateral Family (D4).
- **Reasoning:** The aim is complete coverage of school geometry (D-002, D-019). Each topic keeps the same principles: drag to explore (D-001), watch why (D-023), paired vocabulary (D-003), everyday objects (D-022).
- **Choices the AI made, for author review:**
  1. **Lab order follows the curriculum sections.** The nav now has 16 labs. Lab numbers are taken from each lab's place in the nav, so they no longer need renumbering by hand.
  2. **Circle Basics is a separate lab** rather than more theorems inside Circle Laws.
  3. **The triangle angle sum and exterior angle (C2, C3) stay in Vector Railways**, where they follow from parallel lines.
  4. **Congruence:** choosing SSA always loads an example where two different triangles fit the facts, because that is the case that shows why SSA fails.
  5. **Bearings sit in the Trigonometry lab**, with east and north components worked out by sin and cos.
  6. **Tessellation sits in the Transformations lab**, because any triangle or quadrilateral tiles the plane by half-turns.
  7. **The map is fictional** (Town A, Village B, Port C), so no real place is named.
  8. **Vector proofs:** the midpoint theorem and the diagonals of a parallelogram. Other proofs may matter more for your students.
  9. **Sphere surface area** uses Archimedes' band argument with live numbers; it is a visual explanation, not a full limit proof.
- **Status of the claim "built":** each topic has an interactive lab. This does not mean it has been checked against the official Cambridge O Level or NCTB documents (see [CURRICULUM.md](CURRICULUM.md)), or tested with students (see [RESEARCH.md](RESEARCH.md)).
- **Consequences:** All 65 topics in sections A–L are built; 21 have a visual proof or derivation. Visual proofs remain to be built for 16 topics (listed in the curriculum map). Next: check the syllabus mapping, then college-level topics (section M).
