# P1 Website Iteration Plan

> Date: 2026-07-14  
> Status: Ready to enter P1  
> Scope: Confirm existing changes, consolidate project information, and define the next website iteration sequence.

## 1. Current decision

The portfolio has enough verified evidence to enter P1 and begin website iteration.

P0 is treated as an **evidence-gate pass with tracked fact follow-ups**. Remaining Sign2Text number conflicts, unfinished artifact preparation, and later screenshot collection do not block homepage information architecture. They do block final copy or public release of the affected claims.

The next implementation should change structure and factual framing first. It should not attempt to finish every project page, bilingual content, visual polish, and release QA in one batch.

## 2. Existing website changes to preserve

The current working tree contains user-authored changes. Do not reset, overwrite, or discard them.

### Tracked HTML/CSS changes

Nine tracked files are modified:

- `index.html`
- `project-sign-language.html`
- `project-chi-dashboard.html`
- `project-nlp-models.html`
- `interest-ai-short-film.html`
- `interest-movie-recommendation.html`
- `interest-video-editing.html`
- `interest-guzheng-football.html`
- `style.css`

The current diff is intentionally small:

- All HTML pages update the stylesheet cache key from `portfolio-rhythm` to `no-projector`.
- `style.css` adds stacking context to `.hero` and `.hero-copy` so the Hero content remains above decorative layers.
- No project order, homepage section order, navigation, or substantive project copy has been changed yet.

These changes are compatible with P1 and should remain in place.

### Untracked evidence and planning files

The repository also contains untracked intake documents, reports, slides, and planning files. Treat them as source evidence. Do not move, rename, publish, or delete them during the first website iteration.

Some source artifacts contain private contact details, local server paths, signatures, or course information. They must not be linked publicly without a separate privacy review.

## 3. Audience and site objective

### Primary audience

- Prospective research mentors, PIs, and graduate-program reviewers interested in human-centered AI and interactive systems.

### Secondary audiences

- Research internship and software/AI internship reviewers.
- Technical collaborators.

### Primary visitor action

- Inspect the strongest projects and open evidence-rich detail pages.

### Secondary visitor actions

- Open the CV.
- Visit GitHub.
- Contact Haojun about research collaboration or internship opportunities.

### Working positioning

English:

> I build and study human-centered AI systems that turn model capabilities into usable interactive tools.

Chinese:

> 探索并构建以人为中心的 AI 交互系统，将模型能力转化为可用的交互工具。

Do not lead with equal-weight labels such as `HCI · ML · Systems`. Systems and ML are supporting methods; the central narrative is human-centered interactive systems.

Do not place `Fall 2027 PhD applicant` in the Hero. Graduate-study plans can appear in About or Education after the wording is reviewed. The Hero availability line should support both research and internships.

Working availability:

> Open to research collaborations and internship opportunities in human-centered AI and interactive systems.

## 4. Confirmed project lineup

### Primary Selected Work

#### 1. Sign2Text

- Type: `Ongoing Research Project`
- Homepage role: strongest formal research signal.
- Problem: explore real-time continuous sign-language recognition for accessible communication scenarios.
- Personal contribution: undergraduate team leadership, SwiftUI application implementation, Top-800 vocabulary work, model retraining, and adaptive-stride experiments.
- Evidence currently available: SRTP final report, results document, defense slides, app screenshots, Phoenix evaluation output.
- Safe result statement: on 642 Phoenix test samples, adaptive stride reduced processed clip count from 64,627 to 39,353, a 39.11% reduction in a compute-cost proxy; WER changed from 21.86 for the fixed-stride baseline to 24.18 for the adaptive configuration.
- Boundary: clip count is not measured wall-clock latency, energy consumption, or direct compute time. Real-world recognition quality remains unstable.
- Public link status: do not link the app or ML repository yet.

#### 2. SceneZero

- Type: `Independent continuation of a course-originated project`
- Homepage role: strongest personal direction and individual product-engineering signal.
- Problem: help author-driven AI filmmakers capture multimodal inspiration and develop spatial scene facts into reusable creative inputs.
- Evidence currently available: local Git history, buildable iOS target, ARKit/RealityKit implementation, SwiftData/local-media architecture, product-positioning documents, development logs, and course-to-independent iteration history.
- Verified implementation boundary: the current `SceneZero/SceneZero` target builds successfully for the iOS simulator.
- Course-to-independent evidence: after the course README point, the committed project added roughly 3,251 Swift lines and continued through product repositioning and multiple releases.
- Boundary: SceneZero has technical and product depth but does not yet have a user study or comparative HCI evaluation.
- V2 boundary: `SceneZeroV2` is currently untracked and is not part of the successfully built Xcode target. Do not describe V2-only spatial resolver, local prompt compiler, or creative-advisor features as released or validated.

#### 3. CHI Social Media Research Dashboard

- Type: `Archived HCI Research Tool`
- Homepage role: strongest completed and publicly inspectable research-tool project.
- Problem: support exploration of a tagged corpus of CHI social-media papers through connected overview, Sankey, and detail views.
- Personal contribution: Overview Panel and chart-to-Sankey filtering in a three-person implementation team.
- Evidence currently available: public repository, live demo, public commits, 197-record dataset, and publishable screenshots.
- Boundary: the dataset contains 197 records, tagging was substantially manual, the interface is web-only, and the project is archived.

#### 4. NLP Model Comparison

- Type: `Mentored ML Study`
- Homepage role: early research-development history and experimental-method evidence.
- Problem: compare classical sentiment-classification pipelines on 4,000 IMDb movie reviews.
- Models: Logistic Regression and Random Forest, each evaluated with BOW and TF-IDF.
- Protocol: 70/15/15 train/validation/test split; vectorizers fit on training data; hyperparameters selected with validation data; final test data held out until reporting.
- Verified result: TF-IDF plus Logistic Regression reached approximately 89.3% test accuracy, with AUROC, AUPRC, and F1 also recorded.
- Ownership boundary: the work was mentored and reused parts of a mentor-provided project structure and code ideas. It must not be labelled fully independent research.
- Boundary: limited error analysis, no strong trivial baseline, no neural model evaluation, and no demonstrated reason why the best pipeline performed best.

### Supporting Work

#### MiniSQL

- Type: `Selected Systems Coursework`
- Date: Spring–Summer 2025.
- Scope: team implementation based on a course framework.
- Personal module: disk-backed B+ tree index manager, including insert, search, delete, split, merge, iterator behavior, tests, and debugging.
- Evidence: personal report, code excerpts, tests, and B+ tree debugging narrative; materials are permitted for publication after privacy cleanup.
- Homepage treatment: compact supporting card or technical-foundations entry, not equal visual weight with the four primary projects.

#### Movie Agent

- Type: `Personal Experiment`
- Current treatment: move out of general personal interests, but keep below Selected Work until one defensible agent-orchestration/MCP lifecycle decision and failure-recovery story are documented.
- Safe outcome: working local prototype that produces taste profiles and film recommendations.
- Boundary: Codex-assisted implementation, CrewAI as an existing framework, cookie-based Letterboxd access, unstable APIs, and no recommendation-quality or user-study evidence.

### Not selected

#### Pintos

- Do not place on the homepage in the current iteration.
- Reason: individual contribution remains incomplete, publication permission is uncertain, and unresolved bugs make the evidence weaker than MiniSQL.

## 5. Claims that must be corrected before visual redesign

The current website contains factual drift. Correct these in the first content batch.

### Homepage

- Replace `junior` with the verified current academic context: rising senior / expected graduation June 2027.
- Replace `Software Engineering · HCI · AI Systems` with the working human-centered AI positioning.
- Remove equal-weight `HCI, ML, Systems` focus language.
- Replace `Research Experience` with `Selected Work`.
- Replace the outdated `summer research opportunities` availability statement.
- Move Selected Work before About.
- Remove or redesign the decorative `Frame 01–04` About strip.

### Sign2Text

- Remove `Working app prototype for real-time translation` as an unqualified outcome.
- Replace vague `helped build` and `participated in refining` language with exact personal work.
- Add the compute/accuracy trade-off only with baseline, dataset, unit, and limitation.
- Do not add repository or live-demo links yet.

### CHI Dashboard

- Do not call 197 records a generically `large body` of academic material.
- Add the archived status, dataset size, team context, personal contribution, and known scale limitations.
- Keep the repository and live demo.

### NLP

- Replace `independent project` with `mentored study`.
- Remove unsupported neural-network claims.
- Do not present t-SNE as a successful finding; it was explored but did not provide a useful separation.
- Keep 89.3% only with the dataset size, split, model, vectorizer, and held-out test context.

### SceneZero

- Add a new project card and new detail-page route.
- State that it originated as a mobile-computing course project and continued independently.
- Only claim features from the current buildable target or clearly label V2 work as in development.
- Do not claim improved creativity, efficiency, usability, or prompt quality without evaluation.

## 6. Target homepage information architecture

Use a student-hybrid structure optimized for research review:

1. `Hero`
   - Identity
   - Current academic context
   - One-sentence technical direction
   - `View Selected Work`, `CV`, and `GitHub` actions
2. `Selected Work`
   - Sign2Text
   - SceneZero
   - CHI Dashboard
   - NLP Model Comparison
3. `Research & Experience`
   - Concise roles, institutions, dates, and outputs
4. `Supporting Work`
   - MiniSQL
   - Movie Agent / Experiments
5. `About`
   - Context not already stated in the Hero
6. `Selected Interests`
   - AI short film, video editing, guzheng, and football, kept compact
7. `Contact`
   - Availability, email, GitHub, and CV

Recommended navigation:

- `Work`
- `Research`
- `About`
- `CV`
- `Contact`

Preserve existing project URLs. Add new URLs only for projects that do not yet have pages.

## 7. Implementation sequence

### Batch 0 — Synchronize planning records

Files:

- `PORTFOLIO_REVISION_CHECKLIST.md`
- `P0_REMAINING_INFORMATION_CHECKLIST.md`

Actions:

- Record P0 as evidence-gate passed with tracked fact follow-ups.
- Replace the stale project inventory with the confirmed lineup above.
- Mark P1 as active.
- Move screenshot collection and artifact cleanup to P2/P3 instead of treating them as P1 blockers.

Exit criteria:

- The planning documents no longer contradict the current project ranking or publication boundaries.

### Batch 1 — Homepage structure and factual reset

Primary files:

- `index.html`
- `style.css`

Actions:

- Update metadata, Hero identity, current context, positioning, availability, and calls to action.
- Rename navigation and sections.
- Move Selected Work directly after the Hero.
- Remove duplicate facts and the decorative About film strip.
- Establish the four-primary-project order.
- Add Supporting Work without giving coursework and experiments equal prominence.
- Keep the existing visual system largely intact; add only CSS needed for the new semantic structure.

Exit criteria:

- A visitor can identify Haojun's direction, strongest work, and contact actions without reading About.
- The homepage contains no known false or stale claims.
- Existing user-authored Hero stacking and cache-key changes remain intact.

### Batch 2 — Normalize project-card content

Primary files:

- `index.html`
- `style.css`

Actions:

- Give every primary card the same evidence-preview structure:
  - project type and status
  - problem/artifact sentence
  - exact personal contribution
  - strongest verified outcome or honest artifact state
  - three to five meaningful tags
  - detail-page target
- Use compact supporting cards for MiniSQL and Movie Agent.
- Do not use a technology list as the main evidence.

Exit criteria:

- Every featured project contains one technical decision or mechanism and one inspectable proof path.
- Team projects distinguish team output from personal work.
- No card uses `Featured Project` or `Project` as its only classification.

### Batch 3 — Add SceneZero and supporting routes

New or changed files:

- `project-scenezero.html`
- Optional `project-minisql.html`
- `interest-movie-recommendation.html` or a later renamed stable route
- `style.css`

Actions:

- Create a SceneZero detail-page skeleton using verified current-target evidence.
- Include a course-to-independent-development timeline.
- Explain one architecture decision, one product decision, and the no-user-study boundary.
- Decide whether MiniSQL needs a full page or a compact evidence entry.
- Reframe Movie Agent from a general interest into a personal technical experiment while preserving its current URL unless a redirect strategy is added.

Exit criteria:

- SceneZero has a valid destination with no V2-only claims presented as complete.
- Supporting items do not look equal to primary research projects.

### Batch 4 — Review and approve English copy

Primary files:

- `index.html`
- Four primary project pages
- Supporting project copy

Actions:

- Apply the content model before polishing prose.
- Remove all `What to add later` sections from public-facing pages.
- Use the pattern: constraint/problem → decision → implementation/evaluation → result → remaining limitation.
- Complete a claim-by-claim fact check against P0 evidence.

Exit criteria:

- Every public claim is supported, qualified, or removed.
- Project types, dates, statuses, roles, and limitations are consistent across homepage, detail pages, and CV.

### Batch 5 — Collect and prepare real media

Priority:

1. CHI overview, filtered Sankey, and details screenshots.
2. Sign2Text app, evaluation result, and architecture/pipeline visuals.
3. SceneZero current-target capture flow, AR placement, Lookbook, and prompt output.
4. NLP result table and representative preprocessing/evaluation figure.
5. MiniSQL B+ tree diagram/test/debugging evidence.

Actions:

- Record permission and privacy status for every asset.
- Remove IP addresses, phone numbers, signatures, emails, local paths, private dataset contents, and account cookies.
- Export responsive WebP/AVIF/JPEG assets as appropriate.
- Write descriptive alt text.

Exit criteria:

- Every primary card has a real visual.
- Every detail page has at least one artifact that proves the stated contribution.

### Batch 6 — Build the CHI detail-page pilot

Primary file:

- `project-chi-dashboard.html`

Actions:

- Implement the shared detail-page sequence:
  1. Summary
  2. Context and constraints
  3. Contribution and collaboration
  4. Approach
  5. Key decision and trade-off
  6. Evidence
  7. Outcome and limitations
  8. Artifacts
- Use CHI first because its repository, demo, dataset, status, and personal contribution are already inspectable.
- Convert the successful page structure into reusable HTML/CSS patterns.

Exit criteria:

- CHI is complete enough to serve as the template for the other detail pages.
- No placeholders or internal TODO language are visible.

### Batch 7 — Complete remaining detail pages

Order:

1. Sign2Text
2. SceneZero
3. NLP Model Comparison
4. Supporting work only where evidence justifies a full page

Special gates:

- Sign2Text: resolve `max_stride` 3 versus 4, Top-800 coverage 87.92% versus 89.3%, and the reference pipeline/repository before finalizing those statements.
- SceneZero: keep current-target and V2 evidence separate until V2 is tracked, included in a target, and built/tested.
- NLP: publish the notebook or explain why it remains private; do not imply neural-model comparison.

### Batch 8 — Bilingual layer

Actions:

- Approve the English source copy first.
- Translate approved content into Chinese.
- Select one static-site bilingual strategy and apply it consistently; do not maintain two drifting sets of facts manually without a shared content source or explicit synchronization checklist.
- Preserve stable English URLs unless bilingual routing is intentionally designed.

Exit criteria:

- Language switching is understandable, keyboard accessible, and consistent across homepage and project pages.
- English and Chinese versions contain the same claims, dates, statuses, and limitations.

### Batch 9 — Visual system, responsive behavior, and release QA

Actions:

- Refine typography, spacing, card hierarchy, real-media crops, and project-type/status labels.
- Verify mobile and desktop layouts.
- Verify heading order, keyboard focus, contrast, alt text, reduced motion, and link integrity.
- Optimize images and lazy-load noncritical media.
- Run local HTML/link checks and browser verification.
- Review metadata, favicon, Open Graph information, CV link, and contact details.

Exit criteria:

- No placeholders, unsupported claims, broken links, or private information remain.
- The strongest work is visible immediately after the Hero.
- Every primary project exposes a contribution, technical decision, evidence, outcome, and limitation.

## 8. Immediate next iteration scope

The next coding turn should implement only **Batch 0 and Batch 1**.

This keeps the first change reviewable:

- synchronize planning documents;
- correct stale facts;
- establish the final homepage section order;
- add the provisional project hierarchy;
- preserve current CSS and existing URLs;
- avoid premature detail-page rewrites and final visual polish.

After Batch 1 is reviewed in the browser, proceed to card normalization and new SceneZero routing.

## 9. P1 completion criteria

P1 is complete when:

- [ ] Three to five primary projects are explicitly selected.
- [ ] Project order reflects research relevance and evidence strength.
- [ ] SceneZero is labelled as an independent continuation of a course-originated project.
- [ ] MiniSQL and Movie Agent have a clearly secondary treatment.
- [ ] Pintos is excluded from the current public lineup.
- [ ] Hero, Selected Work, Research/Experience, Supporting Work, About, Interests, and Contact each have a distinct job.
- [ ] Navigation labels match real section content.
- [ ] The strongest work is visible without reading About.
- [ ] Remaining fact conflicts are recorded as P2 copy gates, not silently published.

## 10. Do not do in the next iteration

- Do not delete or reset existing user changes.
- Do not migrate the static site to a framework.
- Do not publish source reports directly before privacy review.
- Do not link the Sign2Text repositories yet.
- Do not claim SceneZeroV2 features as built or validated.
- Do not claim user impact without a study.
- Do not redesign every detail page before the CHI pilot establishes the shared pattern.
- Do not build the bilingual layer before the English factual source is approved.
- Do not deploy before release QA.
