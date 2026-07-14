# Personal Portfolio Revision Checklist

This document tracks the content, evidence, information architecture, UI, and release work required to turn the current framework site into a publishable computer science portfolio.

Work in phase order. Do not begin visual polish before the project lineup, evidence, and copy structure are stable.

## Status legend

- `[ ]` Not started
- `[x]` Complete
- `[-]` Intentionally skipped or not applicable
- `⚠` Requires factual confirmation
- `🔒` Do not publish until resolved

## Working audience and goal

Treat these as provisional until explicitly confirmed.

- **Primary audience:** prospective research mentors and PhD advisors in AI systems, HCI, and creative tools
- **Secondary audiences:** research-internship reviewers and technical collaborators
- **Primary visitor action:** inspect selected projects and their evidence
- **Secondary visitor actions:** open the CV, visit GitHub, or make contact
- **Site model:** scannable homepage plus separate, evidence-rich project pages

## Master progress

| Phase | Deliverable | Status | Blocks |
|---|---|---:|---|
| P0 | Verified facts and project evidence inventory | `[ ]` | All later phases |
| P1 | Final project lineup and homepage information architecture | `[ ]` | P2–P7 |
| P2 | Approved content model and reviewed copy | `[ ]` | P4–P6 |
| P3 | Real project media and technical proof collected | `[ ]` | P4–P6 |
| P4 | Project cards redesigned | `[ ]` | P7 |
| P5 | One complete project-detail template and CHI pilot page | `[ ]` | P6–P7 |
| P6 | Remaining project and interest pages completed | `[ ]` | P7–P8 |
| P7 | Visual system, responsive behavior, and CSS cleanup | `[ ]` | P8 |
| P8 | Accessibility, performance, metadata, and release QA | `[ ]` | Release |

---

## P0 — Verify facts and inventory evidence

### Personal information

- [x] Current academic-year label: **rising senior** (summer after junior year). Do not describe the current status as `junior`.
- [x] Degree: B.S. in Software Engineering, Zhejiang University; expected graduation **June 2027**.
- [x] Preferred Berkeley wording: **Visiting Student, University of California, Berkeley (Aug. 19-Dec. 19, 2025)**.
- [x] Primary technical positioning: **AI systems for creative production, especially tools that help filmmakers turn creative intent into usable workflow artifacts**. HCI is a supporting research lens; ML and systems are methods, not equal hero labels.
- [x] `Systems` will not appear in the hero until a systems project has inspectable code, tests, or a report. Keep it as supporting background only.
- [x] Current availability: use **“Open to research collaborations and doctoral-application conversations in AI systems, HCI, and AI-assisted filmmaking.”** Confirm the intended PhD entry term before adding a year. Replace any dated “summer research opportunities” wording.
- [x] Public contact: `haojun.yeah@gmail.com`; GitHub: `miss1994forever`. Keep `3230103576@gmail.com` off the homepage unless a school address is specifically needed.
- [x] Football is a secondary personal interest: member of the Computer Science women's football team; primarily right back and sometimes midfield. Do not feature team strength or use it as a research narrative.
- [ ] CV/homepage consistency audit: the live copy still says `junior`, uses broad `HCI · AI Systems` positioning, and has project-copy drift. Resolve during P1-P2 after the evidence intake below is complete.

### Claim rules

- [ ] Do not publish an unsupported metric, user count, authorship claim, publication state, or production-use claim.
- [ ] Separate individual work from team output for every team project.
- [ ] Label each project precisely: research, research tool, independent study, course project, or personal project.
- [ ] Add dates and one of: ongoing, completed, archived, or maintained.
- [ ] Replace vague verbs such as `helped`, `worked on`, and `participated in` with exact actions.
- [ ] State limitations rather than implying that a prototype is production-ready.

### Project evidence inventory

Complete one row for every candidate before final project selection.

| Project | Problem | Scope | My contribution | Technical decision | Outcome | Proof links/assets | Publish readiness |
|---|---|---|---|---|---|---|---|
| Sign2Text (Sep. 2025-present) | Explore an iOS workflow for turning sign-language input into readable text. | SwiftUI prototype with camera preview, translation history, dictionary-management UI, settings, and a mocked translation service. The public README says real CV-SLT integration is still planned. | Public commits are attributed to `miss1994forever`; CV states team lead for 3 undergraduates, literature review, app workflow, and vocabulary upload. Exact algorithm contribution still needs a concrete description. | A protocol-based translation service separates the app UI/camera flow from a replaceable model layer; confirm the rationale and actual model boundary. | Inspectable ongoing iOS prototype. No publishable latency, accuracy, or usability result yet. | [`sign2text.app`](https://github.com/miss1994forever/sign2text.app), public commit history, iOS source. Do **not** link `sign2text-ml` yet. | **Qualified only as an ongoing UI/system prototype**; block any real-time-model-performance claim. |
| CHI Dashboard (May-Jun. 2025) | Help researchers explore a tagged corpus of CHI social-media papers through linked visual views. | Three-panel Vue dashboard: overview charts, Sankey relations, and paper details. The published dataset has 197 records spanning 2020-2025 plus 1 undated record. | In a 3-person team, built the Overview Panel (stacked bars and pie charts) and chart-to-Sankey filtering. README attributes the Overview Panel to 马; public commits under `miss1994forever` corroborate chart interaction and filtering work. | Cross-view selection propagates from overview charts to the Sankey view, keeping aggregate and relational exploration connected. Confirm the exact state-management trade-off for the case study. | Public GitHub Pages demo and inspectable source; confirm whether the project should be labelled completed, archived, or maintained. | [Repository](https://github.com/kkzyu/CHI), [live demo](https://kkzyu.github.io/CHI/#/), local dashboard screenshot, public commits. | **Best P5 case-study pilot.** Add real screenshots and state dataset/feature limitations precisely. |
| Movie Agent (Mar. 2026-present) | Recommend films from mood and Letterboxd context while keeping account actions under user control. | Local-first Python/crewAI agent, Node.js Letterboxd MCP server, FastAPI backend, Vue UI, local SQLite history, taste profiles, settings, and tests. | Public repository commits are exclusively attributed to `miss1994forever`; confirm whether any module has outside contributors or major borrowed scaffolding before writing individual ownership copy. | Separates read and write tools; every Letterboxd mutation requires explicit confirmation. Secrets remain local and masked from the browser. | Ongoing, inspectable personal AI system with documented UI and code; no user-study or recommendation-quality claim. | [Repository](https://github.com/miss1994forever/movie-agent), local UI card image, source tree, public commit history. | **Strong Selected Work candidate.** Capture current screens and document one agent/MCP lifecycle decision. |
| NLP Model Comparison (Feb.-Mar. 2024) | Compare sentiment-classification approaches on IMDb movie reviews. | CV reports preprocessing, classical baselines, neural models, tuning, and visual analysis; exact dataset version and experimental protocol are not yet documented. | CV identifies this as an independent project led by a Stanford Ph.D.; clarify supervision, authorship, and exact implementation ownership. | CV reports TF-IDF + Logistic Regression as the best pipeline; the validation/test boundary and leakage controls are unknown. | CV reports 89.3% accuracy plus AUROC, AUPRC, and F1; the statistic is not publish-ready without split and comparison context. | CV only in the current audit. No public repository, notebook, report, or result artifact was found in the linked GitHub account. | **Blocked by experiment context.** Do not feature or surface 89.3% until evidence is collected. |
| Pintos | Course systems work; CV mentions system calls and debugging race conditions. | Unknown. | Exact implemented system calls, bugs, and code ownership unknown. | Unknown. | Unknown. | CV only. | **Exclude from Selected Work** unless code, report, tests, or debugging evidence can be published. |
| MiniSQL | Course database work; CV mentions B+ tree implementation in C++. | Unknown. | Exact B+ tree responsibilities, integration points, and team ownership unknown. | Unknown. | Unknown. | CV only. | **Exclude from Selected Work** unless code, report, tests, or benchmark evidence can be published. |
| Future filmmaking / editing tool | Candidate only; its concrete user, artifact, and current implementation are not yet recorded. | Unknown. | Unknown. | Unknown. | No public evidence yet. | Add only permitted screenshots, repo, design notes, or a short demo after it exists. | **Not eligible for a homepage card yet.** Use the intake form before promoting it. |

### Project-specific fact checks

#### Sign2Text

- [ ] Confirm the research question and intended users.
- [x] Team size: 3 undergraduate students; CV states that Haojun led the undergraduate team and communicated with graduate collaborators and the PI. Specify the recurring leadership duties in the intake form.
- [ ] List the app screens and workflows personally implemented. Public commits support camera, history, dictionary, and theme/settings work, but this must be confirmed in user-facing terms.
- [ ] Clarify the exact contribution to the continuous translation algorithm. Do not use “refined the algorithm” until the method, code boundary, and evidence are named.
- [ ] Confirm whether any latency, accuracy, vocabulary-size, or usability results may be published.
- [x] `sign2text.app` may be linked as an ongoing app prototype. Do not link `sign2text-ml`.
- [ ] 🔒 Remove placeholder author, year, and repository text from the `sign2text-ml` README before featuring it. The public README still contains `yourusername`, `Your Name`, and an unverified 2023 citation.

#### CHI Dashboard

- [x] Published dataset scope: 197 paper records, dated 2020-2025 with 1 undated record; each record has tags for research content, method, and two platform taxonomies. Confirm that this is the final/publishable research corpus before using the count publicly.
- [x] Personal ownership: the repository README assigns the Overview Panel to 马, and public commits under `miss1994forever` document the bar/pie interaction and filtering work. Keep the team context visible.
- [ ] Identify one meaningful interaction or state-management decision to explain, including what was difficult and the trade-off made.
- [x] Live demo: <https://kkzyu.github.io/CHI/#/>.
- [x] Repository: <https://github.com/kkzyu/CHI>.
- [ ] Select screenshots showing overview, Sankey filtering, and details view.
- [ ] State project limitations and whether development is complete.

#### Movie Agent

- [x] Treat as a leading Selected Work candidate rather than an interest. It directly supports the AI-for-film direction.
- [x] Resolve copy drift: current public code documents **DashScope/Qwen**, not Gemini. Do not publish the existing Gemini wording.
- [x] Public commits are exclusively attributed to `miss1994forever` and cover crewAI, web start, history, taste profile, and latest recommendations. Confirm any external contribution or substantial inherited implementation before claiming every component as individual work.
- [x] Documented safety boundary: read tools retrieve Letterboxd context; write tools require explicit confirmation before execution. In the web flow, the UI remains read-only until a user action opens the confirmation dialog.
- [ ] Capture Home, History, Taste Profile, and Settings screens.
- [ ] Document one agent-orchestration or MCP lifecycle decision, including the rationale and failure handling.
- [x] Repository: <https://github.com/miss1994forever/movie-agent>.

#### NLP Model Comparison

- [ ] Confirm whether the work was solo, mentored, or collaborative.
- [ ] Identify the dataset version, size, and train/validation/test split.
- [ ] Document leakage controls and preprocessing choices.
- [ ] List baseline and neural models actually evaluated.
- [ ] Explain the tuning boundary and final test protocol.
- [ ] Contextualize 89.3% with comparison metrics and dataset split.
- [ ] Collect the result table, confusion matrix, error examples, and relevant visualizations.
- [ ] Provide a notebook, report, environment file, or explain why code cannot be public.

#### Pintos / MiniSQL

- [ ] Determine whether code, reports, tests, or diagrams can be published.
- [ ] For Pintos, identify implemented system calls, concurrency bugs, and debugging evidence.
- [ ] For MiniSQL, identify B+ tree ownership, database architecture, and correctness/performance evidence.
- [ ] Select at most one as the primary Systems project unless both have strong, distinct evidence.
- [ ] If neither has inspectable evidence, remove or weaken `Systems` in the homepage positioning.

### P0 evidence still needed from Haojun

Complete [P0_EVIDENCE_INTAKE.md](P0_EVIDENCE_INTAKE.md) before marking P0 complete. The remaining blockers are: a precise Sign2Text algorithm/app contribution; the CHI decision and limits; the complete NLP evaluation protocol and artifacts; any publishable Pintos/MiniSQL proof; and a scoped description of any new filmmaking tool.

### P0 exit criteria

- [ ] Every intended public claim is verified.
- [ ] Every candidate project has a completed evidence-inventory row.
- [ ] No project is selected only to fill visual space.
- [ ] Projects that cannot separate individual ownership are excluded or clearly qualified.

---

## P1 — Finalize project lineup and information architecture

### Project selection

- [ ] Select three to five primary projects.
- [ ] Keep Sign2Text featured only if real technical evidence is available.
- [ ] Keep CHI Dashboard and use it as the first complete case-study pilot.
- [ ] Promote Movie Agent into Selected Work unless superseded by stronger evidence.
- [ ] Demote NLP until its experiment context is complete.
- [ ] Add one Systems project only if it can support the hero positioning.
- [ ] Move creative and personal work below core technical work.

### Recommended homepage order

- [ ] Hero: identity, current context, technical direction, and direct actions.
- [ ] Selected Work: strongest three to five projects.
- [ ] Research / Experience: concise roles, dates, affiliations, and outputs.
- [ ] About: only context not already stated in the hero.
- [ ] Selected Interests: compact and secondary.
- [ ] Contact: current availability, email, GitHub, and CV.

### Structural changes

- [ ] Rename the mixed `Research Experience` project grid to `Selected Work` or an equally accurate label.
- [ ] Remove or redesign the decorative `Frame 01–04` About film strip.
- [ ] Remove duplicated school, major, and focus facts from either the hero or About.
- [ ] Add visible hero actions: `View Selected Work`, `Download CV`, and `GitHub`.
- [ ] Move selected work directly after the hero.
- [ ] Move coursework lower, compress it, or leave it to the CV.
- [ ] Use literal navigation labels such as Work, Research, About, CV, and Contact.
- [ ] Preserve existing project URLs unless there is a strong reason to rename them.

### P1 exit criteria

- [ ] A visitor can find the strongest work without reading the About section.
- [ ] Project order follows audience relevance and evidence strength, not chronology alone.
- [ ] Every homepage section has a distinct job.
- [ ] The navigation matches actual section content.

---

## P2 — Define the content model and review copy

### Hero content model

- [ ] Name.
- [ ] Current role and institution.
- [ ] One concrete technical direction.
- [ ] One sentence describing the problems or artifacts built.
- [ ] Current opportunity/contact status.
- [ ] Primary and secondary CTAs.

Suggested formula:

> I am a [current role] working on [technical domains], especially [problem class]. I [research/build/evaluate] [artifact types].

### Project card content model

- [ ] Real evidence image or result visual.
- [ ] Project type, status, and date.
- [ ] Project title.
- [ ] One sentence naming the problem and artifact.
- [ ] One exact individual contribution.
- [ ] One contextualized result, finding, or completed deliverable.
- [ ] Three to five meaningful tags.
- [ ] Visible `View case study` affordance.

### Project detail content model

- [ ] Summary: problem, artifact, role, outcome, and best visual.
- [ ] Context and constraints.
- [ ] Personal contribution and team collaboration.
- [ ] Architecture, method, experiment, or interaction flow.
- [ ] Key decisions and rejected alternatives.
- [ ] Evidence with captions and interpretation.
- [ ] Outcome, limitations, and current status.
- [ ] Repository, demo, paper, report, poster, slides, or video.
- [ ] Previous/next project navigation.

### Copy-review checklist

- [ ] Replace generic positioning such as “at the intersection of” with a more concrete focus.
- [ ] Remove phrases that describe the interface instead of the work.
- [ ] Avoid repeating a fact in the summary, bullets, and tags.
- [ ] Prefer active, precise verbs: designed, implemented, instrumented, evaluated, reproduced, led, analyzed.
- [ ] Give every number enough context to interpret it.
- [ ] Use consistent tense: present for ongoing work, past for completed work.
- [ ] Use consistent capitalization for HCI, ML, iOS, GitHub, Vue, and project names.
- [ ] Keep the public site in one primary language unless bilingual support is intentionally designed.
- [ ] Review all About, Interests, and Contact copy after core project copy is stable.

### P2 exit criteria

- [ ] Hero and project-card copy fit the approved content model.
- [ ] Every project exposes at least one technical decision and one proof artifact.
- [ ] Copy clearly distinguishes claim, mechanism, evidence, and limitation.
- [ ] No reviewed page contains internal instructions such as `What to add later`.

---

## P3 — Collect and prepare real project media

### General

- [ ] Replace decorative placeholders with real screenshots, result plots, diagrams, terminal output, or short demos.
- [ ] Create semantic filenames by project and purpose.
- [ ] Record source, ownership, and publication permission for each asset.
- [ ] Provide useful alt text and visible captions where interpretation is required.
- [ ] Avoid placing sensitive data, credentials, participant information, or private research material in assets.

### Priority order

- [ ] CHI: dashboard overview, Sankey interaction, and details state.
- [ ] Sign2Text: app workflow, vocabulary upload, and system/model pipeline.
- [ ] Movie Agent: primary UI, recommendation flow, and architecture.
- [ ] NLP: comparison table, confusion matrix, and error analysis.
- [ ] Systems: architecture, tests, traces, or benchmarks if selected.

### Media optimization

- [ ] Convert large screenshots to an appropriate WebP, AVIF, JPEG, or optimized PNG format.
- [ ] Reduce the approximately 2.3 MB tracked Video Editing card image.
- [ ] Review the approximately 976 KB profile image for additional compression.
- [ ] Include explicit width and height attributes.
- [ ] Lazy-load noncritical images.
- [ ] Keep the first meaningful visual fast to load.

### P3 exit criteria

- [ ] Every selected project has at least one real, publishable visual.
- [ ] Every visual supports a claim or improves understanding.
- [ ] No public page depends on placeholder media.

---

## P4 — Redesign project cards

- [ ] Use one shared card structure for all selected projects.
- [ ] Allow featured and standard variants without changing information meaning.
- [ ] Reduce paragraph length and remove duplicated Role/Tools/Outcome lists.
- [ ] Use real images instead of the decorative phone and metric illustrations.
- [ ] Add type, date, and status labels.
- [ ] Keep role/contribution more prominent than the tool list.
- [ ] Show an outcome only when evidence exists.
- [ ] Add a visible case-study affordance even if the whole card is clickable.
- [ ] Provide hover, focus, and pressed states without hiding essential information.
- [ ] Keep title and summary visible on touch devices.
- [ ] Verify equal visual rhythm without forcing equal text length.

### P4 exit criteria

- [ ] A card is understandable without opening the detail page.
- [ ] Cards can be scanned consistently across desktop and mobile.
- [ ] The strongest project is visually prioritized for a content reason.
- [ ] Cards contain no unsupported result or decorative pseudo-data.

---

## P5 — Build the detail-page system using CHI as the pilot

### Shared layout

- [ ] Replace the empty top media block with a real case-study hero.
- [ ] Add a normal top breadcrumb/back link.
- [ ] Remove or reconsider the fixed bottom Back button.
- [ ] Create a readable article column and a compact facts sidebar.
- [ ] Add a table of contents only if the page becomes long enough to need one.
- [ ] Add figure captions and section anchors.
- [ ] Add artifact buttons near the summary and again near the conclusion where useful.
- [ ] Add previous/next project links at the end.

### CHI pilot content

- [ ] Summary with role, team, date, status, repository, and demo.
- [ ] Problem: exploring a labeled body of CHI social-media papers.
- [ ] Data scope and labeling process.
- [ ] Information architecture of overview, relations, and details panels.
- [ ] Personal ownership of overview charts and cross-view filtering.
- [ ] One key technical or interaction decision with trade-offs.
- [ ] Screenshots or walkthrough of filter propagation.
- [ ] Outcome and limitations.
- [ ] Direct links to repository and live demo.

### P5 exit criteria

- [ ] The CHI page can stand alone as a complete technical case study.
- [ ] The template is reusable but does not force all project types into the same evidence structure.
- [ ] The page contains no public TODOs or empty modules.

---

## P6 — Complete remaining pages

### Sign2Text page

- [ ] Use an HCI + ML + iOS case-study structure.
- [ ] Explain users, research context, app flow, model integration, and vocabulary updates.
- [ ] Distinguish research review, team leadership, app development, and algorithm contributions.
- [ ] Add available evaluation and explicitly state missing evaluation.

### Movie Agent page

- [ ] Move or redirect from the current Interest page as appropriate.
- [ ] Use a software-engineering and AI-systems case-study structure.
- [ ] Explain agents, MCP boundary, API/UI architecture, persistence, and confirmation workflow.
- [ ] Show implementation evidence and limitations of local-first operation.

### NLP page

- [ ] Use an ML experiment structure.
- [ ] Document dataset, split, preprocessing, baseline, metrics, tuning, comparison, and errors.
- [ ] Remove `89.3%` from prominent placement until its evaluation context is complete.

### Interests

- [ ] Keep interests visually secondary to technical work.
- [ ] Decide which interests deserve detail pages and which need only a compact card.
- [ ] Do not publish interest pages without real content or media.
- [ ] Replace generic claims about discipline/creativity with specific personal evidence.
- [ ] Keep titles visible instead of replacing them on hover.

### P6 exit criteria

- [ ] All public project pages meet the shared content model.
- [ ] Each project uses the correct evidence pattern for its field.
- [ ] No public interest or project page contains placeholder instructions.

---

## P7 — Refine the visual system and CSS

### Visual hierarchy

- [ ] Retain, revise, or replace the green/cream palette intentionally.
- [ ] Define a compact set of color, typography, spacing, radius, border, and shadow tokens.
- [ ] Reduce the number of equally styled bordered cards.
- [ ] Spend visual emphasis on the hero, selected work, and technical evidence.
- [ ] Use section numbering only when order has real meaning.
- [ ] Keep motion limited to purposeful transitions and reveals.

### Homepage UI

- [ ] Simplify the hero facts/tags so the first viewport is not overloaded.
- [ ] Keep CTA buttons visible without scrolling.
- [ ] Ensure the profile image does not push the main message too far down on mobile.
- [ ] Redesign or remove the About film strip.
- [ ] Give Selected Work stronger hierarchy than Interests and Coursework.
- [ ] Simplify Contact and remove duplicate links where unnecessary.

### Interaction

- [ ] Do not hide card titles on hover or focus.
- [ ] Make hover enhancements optional; essential content must remain visible without hover.
- [ ] Provide visible keyboard focus on all links and controls.
- [ ] Keep touch targets at least comfortably tappable.
- [ ] Respect `prefers-reduced-motion`.

### CSS maintenance

- [ ] Refactor only after the final DOM/component structure is stable.
- [ ] Remove unused selectors and abandoned layout variants.
- [ ] Merge duplicated component rules where doing so improves clarity.
- [ ] Keep responsive rules close to the components they affect or document the breakpoint strategy.
- [ ] Avoid adding a framework unless it solves a demonstrated maintainability problem.

### P7 exit criteria

- [ ] Visual weight matches content importance.
- [ ] The site feels coherent without making every section a card.
- [ ] Desktop and mobile preserve the same information priority.
- [ ] CSS no longer contains rules for removed components.

---

## P8 — Technical and release QA

### Content integrity

- [ ] Search the site for `TODO`, `What to add later`, `Place`, `coming soon`, and placeholder names.
- [ ] Recheck all dates, roles, links, metrics, and status labels.
- [ ] Confirm team projects state individual contribution.
- [ ] Confirm private work does not expose restricted information.

### Accessibility

- [ ] Verify semantic header, nav, main, section/article, aside, and footer usage.
- [ ] Verify one clear `h1` per page and logical heading order.
- [ ] Test keyboard navigation and visible focus.
- [ ] Check color contrast.
- [ ] Verify alt text, decorative-image treatment, and figure captions.
- [ ] Test reduced motion.

### Responsive and interaction QA

- [ ] Test at approximately 320, 375, 768, 1024, 1440, and wide-desktop widths.
- [ ] Check for horizontal overflow and clipped text.
- [ ] Check mobile menu open/close behavior.
- [ ] Check project cards with long titles and summaries.
- [ ] Check detail-page navigation and media scaling.
- [ ] Confirm the first viewport hints at the next section.

### Performance

- [ ] Compress and resize images.
- [ ] Confirm lazy loading for noncritical media.
- [ ] Confirm font loading does not block essential readability.
- [ ] Review the external Motion dependency and ensure content remains usable if it fails.
- [ ] Check for console errors and missing assets.

### Metadata and sharing

- [ ] Add a unique meta description to every public detail page.
- [ ] Add canonical URLs.
- [ ] Add Open Graph and social-preview metadata.
- [ ] Verify page titles and favicon.
- [ ] Add or verify `robots.txt` and sitemap if appropriate.
- [ ] Ensure stable GitHub Pages/custom-domain paths.

### Link and artifact QA

- [ ] Test every local and external link without relying on an authenticated session.
- [ ] Link directly to live demos, repositories, reports, or relevant subdirectories.
- [ ] Confirm the CV opens correctly.
- [ ] Confirm repository READMEs include purpose, setup, demo, testing, status, and limitations.

### Release gate

- [ ] No visible placeholder or internal instruction remains.
- [ ] Every featured project has a problem, contribution, technical decision, outcome, and proof.
- [ ] A 30-second reviewer can identify the technical direction and strongest project.
- [ ] Desktop and mobile screenshots have been reviewed.
- [ ] Available validation/build checks pass.
- [ ] The deployed custom domain and GitHub Pages URL both work as intended.

---

## Do not prioritize yet

- [ ] Do not add more animation before content hierarchy is stable.
- [ ] Do not migrate frameworks solely for visual redesign.
- [ ] Do not perfect every interest page before the selected technical work is complete.
- [ ] Do not add generic skill bars, proficiency percentages, or technology-logo clouds.
- [ ] Do not publish decorative charts that look like evaluation evidence.
- [ ] Do not add weak projects to make the grid symmetrical.

## Decision log

Record decisions that affect later work so they are not repeatedly reopened.

| Date | Decision | Reason | Affected pages |
|---|---|---|---|
| 2026-07-10 | Lead with AI systems for creative production and AI-assisted filmmaking; use HCI as a supporting research lens. | Matches current research direction and intended PI/PhD audience without overclaiming a finished filmmaking product. | Homepage, CV summary, project ordering |
| 2026-07-10 | Do not use Systems as a hero label until Pintos or MiniSQL has inspectable evidence. | Current audit found only CV claims, not public code, tests, reports, or benchmarks. | Homepage hero, About |
| 2026-07-10 | Keep football and guzheng secondary; do not make them a featured narrative. | They are personal interests, not evidence for the research positioning. | Interests, About |
| YYYY-MM-DD |  |  |  |

## Content source log

Use this to track the source behind important claims.

| Claim or asset | Source | Permission/status | Last verified |
|---|---|---|---|
| Zhejiang University degree, expected June 2027 graduation, Berkeley attendance | CV + personal confirmation | Public biographical claim | 2026-07-10 |
| Berkeley dates: Aug. 19-Dec. 19, 2025 | Personal confirmation | Public biographical claim | 2026-07-10 |
| AI-for-filmmaking research direction and contact details | Personal confirmation | Public positioning/contact claim | 2026-07-10 |
| Sign2Text app architecture and ongoing-model status | `miss1994forever/sign2text.app` README, source tree, and commits | Public repository; model-performance claims not permitted | 2026-07-10 |
| CHI role, source, demo, and dataset scope | `kkzyu/CHI` README, commits, published dataset, and live demo | Public repository/demo; retain team attribution | 2026-07-10 |
| Movie Agent architecture, safety boundary, and authorship evidence | `miss1994forever/movie-agent` README, source tree, and commits | Public repository; no quality/user-study claim | 2026-07-10 |
| NLP, Pintos, and MiniSQL summaries | CV only | Not sufficient for feature claims; requires project evidence | 2026-07-10 |
