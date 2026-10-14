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
- **Origin:** AI proposal, built at the author's request; details pending author review
- **Decision:** One lab, placed first in the navigation, with seven stations matching curriculum topics A1–A7. Each station pairs a hands-on figure with paired vocabulary (D-003) and an everyday-objects card (D-022).
- **Pending author review:**
  1. **Everyday examples.** These are AI-drafted, and some were chosen to be familiar in Bangladesh: a samosa, a carrom board, a paper kite (ghuri), the national flag. Replace any that do not fit your students.
  2. **Emoji or illustrations.** Everyday objects are currently shown with emoji. Purpose-made illustrations or photographs would be clearer and more culturally specific, but they need design work or a budget.
  3. **The trapezium definition.** The shape sorter calls a four-sided shape with *exactly one* pair of parallel sides a trapezium. Some curricula use "at least one pair", which also counts parallelograms. Match this to the curriculum you teach.
  4. **Lab names.** "Foundations" (Lab 1) and "Foundation Runway" (Lab 2) sound alike. Consider renaming one.
- **Consequences:** Topics A1–A7 are now built (see [CURRICULUM.md](CURRICULUM.md)).

## D-026 · Counting faces, edges and vertices on curved solids
- **Date:** 2026-10-14
- **Origin:** AI proposal, pending author review
- **Decision:** Curved surfaces are counted as faces, and listed separately from flat faces. Circular rims count as edges. The tip of a cone counts as a vertex. Cylinder: 2 flat + 1 curved face, 2 edges, 0 vertices. Cone: 1 flat + 1 curved, 1 edge, 1 vertex. Sphere: 1 curved surface, 0 edges, 0 vertices.
- **Reasoning:** This is the most common school convention, but textbooks disagree. Some say a cone has no vertex, or that only flat surfaces count as faces. The lab therefore keeps Euler's pattern to flat-faced solids only.
- **Consequences:** If the author's curriculum uses another convention, change the counts in `src/labs/foundations/Solids3D.jsx`.
