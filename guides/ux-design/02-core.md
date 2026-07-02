# Goal 2: core UX skills - research, IA, wireframes, accessibility meow

> **~170h total** - your pace, no deadline.
> goal: learn the actual UX process, not just how to make pretty screens.
> this is where your portfolio starts getting evidence behind it.

[Previous: Goal 1](01-foundations.md) - [Hub](README.md) - [Next: Goal 3](03-specialization.md)

---

- [ ] **user research** (~60h)
- [ ] **information architecture** (~40h)
- [ ] **wireframing: lo-fi -> hi-fi** (~30h)
- [ ] **interaction design + microinteractions** (~20h)
- [ ] **accessibility with WCAG 2.2** (~15h)
- [ ] **design systems + components** (~5h)
- [ ] **exit check** - real usability test, IA artifacts, accessible design, mini system

## user research (~60h)

research is the part generative AI cant do for u.
it is also what hiring managers most want to see evidence of in junior case studies.

### what to cover

- [ ] **Research planning:** define what decision the research will inform before scheduling anything.
- [ ] **Moderated usability testing:** 5 participants catch about 85% of usability issues. recruit, write a protocol, facilitate without leading, take notes.
- [ ] **User interviews:** semi-structured interviewing. ask "tell me about a time when..." instead of "would u use X?"
- [ ] **Surveys:** useful for scale and prevalence, weak for understanding why. know Likert scales, closed vs open questions, and leading-question traps.
- [ ] **Card sorting:** open and closed sorts help inform information architecture.
- [ ] **Tree testing:** validates IA structure before building.
- [ ] **Affinity mapping:** synthesize qualitative data into themes in FigJam.
- [ ] **Jobs to Be Done (JTBD):** "When I [situation], I want to [motivation], so I can [outcome]."
- [ ] **Research ethics:** informed consent, privacy basics, and avoiding harm to vulnerable participants.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| Conduct a 3-person usability test on any existing app | in-person or video call | write a test plan, recruit 3 participants, run sessions, and write a 1-page synthesis with top 3 findings | **Free** |
| Affinity mapping exercise | FigJam | cluster usability notes into themes with sticky notes and produce a portfolio-ready board screenshot | **Free** |
| [Nielsen Norman Group free articles](https://www.nngroup.com/articles/) | Web | read "Why You Only Need to Test with 5 Users," "Card Sorting," and "How to Conduct a User Interview" | **Free** |
| [Optimal Workshop learn library](https://www.optimalworkshop.com/learn/) | Web | read IA/card-sort guides and run the free tree-testing trial on a navigation u want to evaluate | **Free** |

junior portfolio trap: "i conducted interviews" is not enough.
show what u learned, show the synthesis, and connect at least one finding to a design decision.

**practice gate:** u can plan and facilitate a 30-minute usability test, synthesize 3-5 insights, and explain how at least one insight changed a design decision.

## information architecture (~40h)

information architecture (IA) is how u organize, label, and structure content so users can find things.
good IA is invisible.
bad IA is painful.

### what to cover

- [ ] **Navigation patterns:** global nav, local nav, breadcrumbs, tabs, hamburger menus.
- [ ] **Content hierarchies:** translate a content inventory into a tree structure.
- [ ] **Labeling:** write navigation labels users recognize, not internal jargon.
- [ ] **Site maps:** document product structure as a diagram in Figma or FigJam.
- [ ] **Flows and task flows:** show the sequence a user follows to complete a task.
- [ ] **Mental models:** users bring expectations from other products. your IA should not mirror the org chart unless the org chart matches user thinking.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| Site map exercise | FigJam | pick any 10-page website and reverse-engineer its IA into a site map diagram | **Free** |
| User flow exercise | Figma | design a complete task flow with 5-8 steps and decision branches | **Free** |
| Card sort on your portfolio site | FigJam | write planned portfolio sections on stickies and ask 3 people to group them | **Free** |

**practice gate:** u can produce a site map and task-flow diagram for a product, then explain how a card sort result would change the navigation labels.

## wireframing: lo-fi -> hi-fi (~30h)

wireframing is thinking made visible.
do it before u touch color, even when u really want to skip ahead.

### what to cover

- [ ] **Lo-fi wireframes:** grayscale, low detail, paper or Figma shapes. test layout and flow, not aesthetics.
- [ ] **Mid-fi wireframes:** precise layout, real content, consistent spacing, no final color or imagery.
- [ ] **Hi-fi mockups:** pixel-accurate screens with color, typography, imagery, and component states. built on Goal 1.
- [ ] **Fidelity decisions:** know why u chose each fidelity level.
- [ ] **Annotation:** explain interaction behavior, states, and edge cases so developers can read the file.
- [ ] **Responsive considerations:** design at least mobile and desktop. they are usually not the same layout.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| Lo-fi -> hi-fi walkthrough | Figma | pick a Daily UI prompt, sketch lo-fi in 20 min, build mid-fi, then apply your Goal 1 color and type system | **Free** |
| Annotation practice | Figma | add a full annotation layer to one wireframe: interactions, states, responsive notes | **Free** |
| [Flux Academy on YouTube](https://www.youtube.com/@FluxAcademy) | YouTube | watch "UI Design Process" and "From Wireframe to Design," then rebuild the example - ⚠️ TODO verify exact videos | **Free** |

**practice gate:** u can produce lo-fi, mid-fi, and hi-fi versions of the same screen and explain the purpose and audience of each fidelity.

## interaction design + microinteractions (~20h)

how things move and respond is part of the design.
interactions communicate state, provide feedback, and build confidence.

### what to cover

- [ ] **Feedback and system status:** every user action needs a response. silence is a UX bug.
- [ ] **Microinteractions:** small purposeful animations, like checkbox feedback or a like-button pulse.
- [ ] **Transition types:** instant, fade, slide, smart animate. each has a different cognitive effect.
- [ ] **Timing:** 100-300ms is the sweet spot for UI feedback.
- [ ] **Error prevention and recovery:** prevent errors first. if an error happens, tell the user what to do next.
- [ ] **Empty states:** no-data screens need a clear call to action.
- [ ] **Destructive action patterns:** confirmation dialogs, undo/redo, soft-delete.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| Microinteraction prototype | Figma | build a button with default, hover, loading, and success states using prototyping and smart animate | **Free** |
| Form error states | Figma | design a 3-field form with empty-submit, invalid-format, and server-error states, all annotated | **Free** |
| [ProtoPie trial](https://www.protopie.io) | ProtoPie | build one sensor/logic-driven interaction, like swipe-to-delete with spring animation, in the free watermarked tier | Free (watermarked) |

**practice gate:** u can prototype a form with empty, loading, error, and success states in Figma and explain the timing choices.

## accessibility with WCAG 2.2 (~15h)

accessibility isnt a checklist bolt-on.
its part of designing correctly, mhm.

WCAG 2.2 organizes requirements under four principles: **Perceivable, Operable, Understandable, Robust** (POUR).

- [ ] **Perceivable:** information must be presentable to all senses. color is never the only differentiator.
- [ ] **Operable:** all functionality must be keyboard-accessible. focus order must be logical. touch targets should be usable.
- [ ] **Understandable:** language and behavior must be predictable. forms need visible, persistent labels.
- [ ] **Robust:** designs must be implementable in semantic HTML that works with assistive technology.

key WCAG 2.2 success criteria designers own:

- [ ] **1.4.3 Contrast (AA):** 4.5:1 for normal text, 3:1 for large text.
- [ ] **1.4.11 Non-text contrast:** 3:1 for UI component boundaries.
- [ ] **2.4.11/12 Focus appearance:** focus indicators must be visible and meet area/contrast requirements.
- [ ] **2.5.8 Target size:** interactive targets >= 24x24px minimum.

knowing WCAG exists isnt enough.
use tools that check it.
Stark catches many design-layer issues before code exists.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| Accessibility audit | Figma + Stark | take a Goal 1 design, run a full Stark audit, fix every flagged issue, and document before/after | **Free** |
| Color-blindness simulation | Stark | view portfolio screens through each color-blindness mode and fix any lost information | **Free** |
| Keyboard flow annotation | Figma | annotate a 3-screen flow with tab order numbers and focus state designs | **Free** |

**practice gate:** u can run a Stark audit, fix all WCAG 2.2 AA contrast failures, and annotate focus order for a form.

## design systems + components (~5h)

design systems are the infrastructure that lets a product scale.
junior-level fluency here signals professional maturity.

### what to cover

- [ ] **Design system:** shared components, styles, tokens, and documentation. not just a UI kit.
- [ ] **Design tokens:** named values for color, spacing, typography, radius. bridge between design and code.
- [ ] **Component anatomy:** base component -> variants -> states.
- [ ] **Pattern libraries vs component libraries:** patterns are larger behaviors, components are reusable building blocks.
- [ ] **Contributing to a system:** use an existing system correctly and propose additions carefully.
- [ ] **References:** study [Material Design 3](https://m3.material.io) and [Apple Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines).

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| Build a mini design system | Figma | create color tokens, a type scale, and 5 components: button, input, card, badge, toast, each with variants and states | **Free** |
| Audit an existing system | Figma Community | duplicate a community UI kit, identify 3 inconsistencies or missing states, and write a 1-paragraph proposal for each | **Free** |

**practice gate:** u can build a 5-component Figma library with consistent tokens, variants, and states, then explain the naming convention.

## exit check

- [ ] conducted at least one real usability test with 3+ participants
- [ ] produced an affinity map and written research synthesis
- [ ] built a site map and a task-flow diagram for a real product
- [ ] produced lo-fi, mid-fi, and hi-fi versions of the same screen
- [ ] designed all form states: default, error, loading, success
- [ ] fixed a Figma design to pass WCAG 2.2 AA contrast for all text and UI components
- [ ] built a mini design system with tokens + 5 components in Figma

[Next: Goal 3 - Pick Your Track](03-specialization.md)
