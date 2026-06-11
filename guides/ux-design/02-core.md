# 🔬 Phase 2: Core UX Skills

> **~170 hrs total** · your pace, no deadline
> The full UX process: research, information architecture, wireframing, interaction design, accessibility, and design systems.

[← Phase 1](01-foundations.md) · [Hub](README.md) · [Next: Phase 3 — Specialization →](03-specialization.md)

---

## User Research (~60 hrs)

Research is the part generative AI can't do for you — and it's what hiring managers most want to see evidence of in your case studies.

### What to cover

- **Research planning:** a research question isn't the same as "let's talk to users." Define what decision the research will inform before scheduling a single session.
- **Moderated usability testing:** 5 participants catch ~85% of usability issues (Nielsen's rule). How to recruit, write a protocol, facilitate without leading, take notes.
- **User interviews:** semi-structured interviewing technique. Ask "tell me about a time when..." not "would you use X?" — behavior over opinion.
- **Surveys:** when they make sense (scale, quantitative signal) and when they don't (understanding *why*). Likert scales, closed vs open questions, avoiding leading questions.
- **Card sorting (open and closed):** how to run a card sort to inform information architecture. Tools: OptimalSort (freemium), or a Figma/FigJam card sort.
- **Tree testing:** validating IA structure before building. Related to card sorting.
- **Affinity mapping:** synthesizing qualitative data into themes. Do this in FigJam.
- **Jobs to Be Done (JTBD):** "When I [situation], I want to [motivation], so I can [outcome]." A useful frame for understanding user goals without feature-anchoring.
- **Research ethics:** informed consent, data privacy basics, avoiding harm to vulnerable participants.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Conduct a 3-person usability test on any existing app | In-person or video call | Write a test plan, recruit 3 participants (friends/family is fine), run the sessions, and write a 1-page synthesis with top 3 findings | **Free** |
| Affinity mapping exercise | FigJam | Take your usability test notes and cluster them into themes using sticky notes — produce a FigJam board you can screenshot for your portfolio | **Free** |
| [Nielsen Norman Group — free articles](https://www.nngroup.com/articles/) | Web | Read "Why You Only Need to Test with 5 Users," "Card Sorting," and "How to Conduct a User Interview" | **Free** |
| [Optimal Workshop blog](https://www.optimalworkshop.com/learn/) | Web | Read their IA and card-sort guides; run the free tree-testing trial on a navigation you want to evaluate | **Free** |

> **The research documentation trap:** a lot of junior portfolios show a research section that says "I conducted interviews" but don't show what was learned or how it changed the design. Show the synthesis (affinity map, key insights) and explicitly connect it to a design decision.

**Practice gate:** you can plan and facilitate a 30-minute usability test, synthesize findings into 3–5 insights, and explain how at least one insight changed a design decision before moving on.

---

## Information Architecture (~40 hrs)

Information architecture (IA) is how you organize, label, and structure content so users can find things. Good IA is invisible; bad IA is painful.

### What to cover

- **Navigation patterns:** global nav, local nav, breadcrumbs, tabs, hamburger menus — when each is appropriate.
- **Content hierarchies:** how to translate a content inventory into a tree structure.
- **Labeling:** writing navigation labels users actually recognize (not internal jargon). Card sorts reveal this.
- **Site maps:** documenting the structure of a product as a diagram. You'll build these in Figma or FigJam.
- **Flows and user task flows:** how a user moves through a product to complete a task. This is distinct from a sitemap (structure) — flows show sequences.
- **Mental models:** users have pre-existing expectations from other products. Your IA needs to match their mental model, not your org chart.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Site map exercise | FigJam | Pick any 10-page website and reverse-engineer its IA into a site map diagram | **Free** |
| User flow exercise | Figma | Design a complete task flow (5–8 steps: e.g., "sign up and complete profile") with decision branches | **Free** |
| Card sort on your own portfolio site | FigJam | Write your planned portfolio sections on stickies and ask 3 people to group them — does the grouping match your mental model? | **Free** |

**Practice gate:** you can produce a site map and a task-flow diagram for a given product and explain how a card sort result would change the navigation labels before moving on.

---

## Wireframing: Lo-Fi → Hi-Fi (~30 hrs)

Wireframing is thinking made visible — do it before you touch color.

### What to cover

- **Lo-fi wireframes:** grayscale, low-detail sketches (paper or Figma with basic shapes). The goal is to test layout and flow, not aesthetics. Speed matters — don't spend more than 20 minutes on a lo-fi screen.
- **Mid-fi wireframes:** more precise layouts, real content, consistent spacing, but no color or imagery. This is where you validate structure with stakeholders before investing in hi-fi.
- **Hi-fi mockups:** pixel-accurate screens with color, typography, real imagery, component states. Built on your Phase 1 foundations.
- **Fidelity decisions:** know *why* you chose a fidelity level. Showing lo-fi to test layout is correct; showing lo-fi to test visual appeal is not.
- **Annotation:** labels on wireframes explaining interaction behavior, states, and edge cases. Developers read these.
- **Responsive considerations:** design for at least two breakpoints (mobile and desktop) — they're usually not the same layout.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Lo-fi → hi-fi walkthrough | Figma | Pick any Daily UI prompt; sketch lo-fi in 20 min, build mid-fi layout, then apply your Phase 1 color and type system to produce hi-fi | **Free** |
| Annotation practice | Figma | Take one existing wireframe and add a full annotation layer: interaction notes, states, responsive notes | **Free** |
| [Flux Academy on YouTube](https://www.youtube.com/@FluxAcademy) | YouTube | Watch "UI Design Process" and "From Wireframe to Design" — rebuild the example | **Free** |

**Practice gate:** you can produce lo-fi, mid-fi, and hi-fi versions of the same screen and explain the purpose and intended audience of each fidelity before moving on.

---

## Interaction Design & Microinteractions (~20 hrs)

How things move and respond is part of the design. Interactions communicate state, provide feedback, and build confidence.

### What to cover

- **Feedback and system status:** every user action needs a response — button loading states, success confirmations, error messages. Silence is a UX bug.
- **Microinteractions:** small, purposeful animations. A checkbox that "checks" with a bounce, a like button that pulses — these signal responsiveness and add delight without clutter.
- **Transition types:** instant, fade, slide, smart animate (Figma's morph between similar layers). Each has a different cognitive effect.
- **Timing:** 100–300ms is the sweet spot for UI feedback. Longer feels broken; shorter feels imperceptible.
- **Error prevention and recovery:** the best error message is the one that never appears (prevent the error). The second-best is clear, specific, and tells the user what to do next.
- **Empty states:** what does a screen look like when there's no data? Empty states with a clear call to action are better than a blank void.
- **Destructive action patterns:** confirmation dialogs, undo/redo, soft-delete — protect users from mistakes.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Microinteraction prototype | Figma | Build a button with 4 states (default, hover, loading, success) using Figma prototyping and smart animate | **Free** |
| Form error states | Figma | Design a 3-field form with all error states: empty submit, invalid format, server error — all annotated | **Free** |
| [ProtoPie trial](https://www.protopie.io) | ProtoPie | Build one sensor/logic-driven interaction (e.g., a swipe-to-delete with spring animation) in the free watermarked tier | Free (watermarked) |

**Practice gate:** you can prototype a form with empty, loading, error, and success states in Figma and explain the timing choices for each transition before moving on.

---

## Accessibility (WCAG 2.2) (~15 hrs)

Accessibility isn't a checklist bolt-on — it's part of designing correctly.

### What to cover

WCAG 2.2 organizes requirements under four principles: **Perceivable, Operable, Understandable, Robust** (POUR).

- **Perceivable:** information must be presentable to all senses. Text alternatives for images (alt text), captions for video. Color is never the *only* differentiator — add icons, labels, or patterns.
- **Operable:** all functionality must be keyboard-accessible. Focus order must be logical. Touch targets ≥ 44×44px. No interaction that requires hover only.
- **Understandable:** UI language and behavior must be predictable. Error messages must describe the problem and the fix in plain language. Forms must have visible, persistent labels.
- **Robust:** designs must be implementable in semantic HTML that works with assistive technology (screen readers, switch access).

Key WCAG 2.2 success criteria designers own:
- **1.4.3 Contrast (AA):** 4.5:1 for normal text, 3:1 for large text (18px+ bold / 24px+ regular).
- **1.4.11 Non-text contrast:** 3:1 for UI component boundaries (buttons, inputs).
- **2.4.11/12 Focus appearance (new in 2.2):** focus indicators must be visible and meet minimum area/contrast.
- **2.5.8 Target size (new in 2.2):** interactive targets ≥ 24×24px minimum.

> Knowing WCAG exists isn't enough. You need to use the tools that check it. The Stark plugin catches most common design-layer issues before code is written.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Accessibility audit | Figma + Stark | Take a Phase 1 design, run a full Stark audit, and fix every flagged issue — document before/after | **Free** |
| Color-blindness simulation | Stark | View your portfolio case study screens through each color-blindness mode; identify and fix any information lost | **Free** |
| Keyboard flow annotation | Figma | Annotate a 3-screen flow with tab order numbers and focus state designs | **Free** |

**Practice gate:** you can run a Stark accessibility audit on a Figma file, fix all WCAG 2.2 AA contrast failures, and annotate the focus order for a form before moving on.

---

## Design Systems & Components (~5 hrs)

Design systems are the infrastructure that scales a product. Understanding them at a junior level signals professional maturity.

### What to cover

- **What a design system is:** a shared library of components, styles, tokens, and documentation. It's not a UI kit — it's a living product.
- **Design tokens:** named values for color, spacing, typography, border-radius. Tokens are the bridge between design and code.
- **Component anatomy:** base component → variants → states. A button isn't one element; it's a system of related variants.
- **Pattern libraries vs component libraries:** patterns are higher-level (a search pattern might include an input, a button, a results list); components are the reusable building blocks.
- **Contributing to a system:** you won't build a design system from scratch on day one, but you'll be expected to use one correctly and propose additions. Show you understand the governance model.
- **Real-world reference:** study [Material Design 3](https://m3.material.io) and the [Apple Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines) — both free and publicly documented.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Build a mini design system | Figma | Create a component library with: a color token set, a type scale, and 5 components (button, input, card, badge, toast) each with full variants and states | **Free** |
| Audit an existing system | Figma Community | Duplicate a community UI kit, identify 3 inconsistencies or missing states, and write a 1-paragraph proposal for each | **Free** |

**Practice gate:** you can build a 5-component Figma library with consistent tokens, variants, and states — and explain the naming convention you used and why before moving on.

---

## Phase 2 exit checklist

- [ ] Conducted at least one real (not made-up) usability test with 3+ participants
- [ ] Produced an affinity map and written research synthesis
- [ ] Built a site map and a task-flow diagram for a real product
- [ ] Produced lo-fi, mid-fi, and hi-fi versions of the same screen
- [ ] Designed all form states: default, error, loading, success
- [ ] Fixed a Figma design to pass WCAG 2.2 AA contrast for all text and UI components
- [ ] Built a mini design system with tokens + 5 components in Figma

Next: [Phase 3 — Specialization (Product Designer, UX Researcher, UI Designer, Content Designer) →](03-specialization.md)
