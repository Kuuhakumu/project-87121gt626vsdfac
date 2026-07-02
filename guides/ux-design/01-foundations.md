# Goal 1: foundations - visual design, color, type, Figma meow

> **~130h total** - your pace, no deadline.
> goal: learn the visual grammar before u try to build serious UX case studies.
> this is where the screens stop looking random qwq.

[Previous: Goal 0](00-prep.md) - [Hub](README.md) - [Next: Goal 2](02-core.md)

---

- [ ] **visual design principles** (~40h)
- [ ] **color theory + typography** (~40h)
- [ ] **Figma fundamentals** (~50h)
- [ ] **exit check** - accessible palette, type scale, auto layout, Daily UI reps

## visual design principles (~40h)

visual design is a language with rules.
learn them before u break them.

### what to cover

- [ ] **Hierarchy:** the eye reads in order. size, weight, contrast, and position direct attention.
- [ ] **Contrast:** differences in lightness, color, size, and shape create emphasis. low contrast is the most common beginner mistake.
- [ ] **Alignment:** invisible grid lines hold a layout together. misalignment reads as carelessness.
- [ ] **Proximity:** related elements belong together, unrelated elements need space.
- [ ] **White space:** negative space is not wasted space. it reduces cognitive load and makes the layout feel calmer.
- [ ] **Repetition:** consistent visual patterns create unity. design systems are formalized repetition.
- [ ] **Scale and proportion:** size relationships between headings, body copy, buttons, and icons communicate importance.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [Sharpen.design](https://sharpen.design) | Web | generate random UI prompts and apply each principle deliberately | **Free** |
| Figma fundamentals (in-app tutorial) | Figma | complete the official "Figma for beginners" 4-part tutorial and apply layout principles | **Free** |
| [DesignCourse on YouTube](https://www.youtube.com/@DesignCourse) | YouTube | watch the "UI Design Fundamentals" series and recreate 3 examples in Figma - ⚠️ TODO verify exact playlist/video | **Free** |
| [Refactoring UI free preview](https://www.refactoringui.com) | Web | read the free preview and apply hierarchy + spacing techniques to a blank card component | **Free** |

**practice gate:** u can look at any UI, spot at least 3 hierarchy or layout problems, and explain why they are problems before moving on.

## color theory + typography (~40h)

these two systems carry most of a design's emotion and readability.
dont skip them bc Figma feels more fun meow.

### color theory

- [ ] **Color models:** HSL is how u think about color in UI. RGB and hex are how u implement it.
- [ ] **Color wheel basics:** complementary, analogous, triadic schemes. complementary usually works better as an accent than a 50/50 split.
- [ ] **Saturation and lightness:** most beginner color mistakes are over-saturated. professional palettes use muted, shifted tones.
- [ ] **Semantic color:** red means error/destructive, green means success. consistency is a usability feature.
- [ ] **Accessibility:** color alone must never be the only signal. WCAG 2.2 minimum contrast ratios: 4.5:1 for normal text, 3:1 for large text and UI components.
- [ ] **Building a palette:** one neutral scale + one brand color + success/error semantic colors covers most UI needs.

### typography

- [ ] **Type anatomy:** baseline, x-height, ascenders, descenders, kerning, tracking, leading.
- [ ] **Type scale:** modular scales, like 1.25 or 1.333, make heading/body relationships consistent.
- [ ] **Font pairing:** one display or heading font + one body font is the safe default.
- [ ] **Variable fonts:** useful for reducing load in web UI. know they exist.
- [ ] **Readability rules:** body copy 15-20px, line-height 1.4-1.6, line length 60-75 characters.
- [ ] **Choosing typefaces:** system fonts like Inter, SF Pro, and Roboto are workhorses. Google Fonts are fine for early projects.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [Coolors.co](https://coolors.co) | Web | generate 5 accessible UI color palettes and check each with WebAIM Contrast Checker | **Free** |
| [Google Fonts](https://fonts.google.com) | Web | build a type specimen in Figma: heading, subheading, body, caption with a modular scale | **Free** |
| [Typescale.com](https://typescale.com) | Web | try 3 ratios and export a scale for your Goal 4 case study | **Free** |
| Figma color styles exercise | Figma | create a local color style library: neutral scale + brand color + success/error/warning tokens | **Free** |

color and accessibility are not separate concerns.
use Stark every time u make a color decision, even if it feels slow at first.

**practice gate:** u can build a 5-color accessible UI palette from scratch, verify every text/background combo meets WCAG 2.2 AA, and explain why each color was chosen.

## Figma fundamentals (~50h)

Figma is the default design and prototyping tool.
learn it deeply enough that the tool stops interrupting your thinking.

### what to cover

- [ ] **Frames vs groups:** frames are the building block of layouts. groups are quick organization.
- [ ] **Auto layout:** Figma's flexbox-like system for responsive components. fill/hug/fixed is where most beginners get stuck.
- [ ] **Components and variants:** one button with states should be one component with variants, not four separate frames.
- [ ] **Styles and variables:** text styles, color styles, effect styles, and variables for design tokens.
- [ ] **Prototyping:** link frames with interactions. know instant, dissolve, and smart animate.
- [ ] **Dev Mode:** know how a developer reads your Figma file, measurements, and tokens.
- [ ] **Plugins:** Stark, Unsplash, Iconify. keep the early plugin list short.

**Figma pricing reality:** the free Starter tier is 1 team, 3 Figma files, unlimited FigJam.
when the 3-file limit gets annoying, archive old projects or use Penpot for overflow.
u dont need Pro to learn.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [Figma "Explore design" tutorials](https://www.figma.com/resources/learn-design/) | Figma | complete Components, Auto layout, and Prototyping modules, then publish a component set to a community file | **Free** |
| [Figma Community](https://www.figma.com/community) | Figma | duplicate a mobile app UI kit and redesign one screen using its component library | **Free** |
| [Jesse Showalter on YouTube](https://www.youtube.com/@JesseShowalter) | YouTube | watch the Figma auto-layout deep dive and rebuild the example from scratch - ⚠️ TODO verify exact video | **Free** |
| [Daily UI](https://www.dailyui.co) | Web/email | complete Days 1-10 as Figma frames with real auto layout and components | **Free** |

**practice gate:** u can build a mobile app screen with auto layout, a button component with 3 variants, and a working prototype flow with at least 3 linked screens.

## exit check

- [ ] can identify hierarchy, contrast, alignment, and proximity issues in any UI
- [ ] built a 5-color accessible palette with verified contrast ratios
- [ ] built a type scale, from heading to body to caption, as Figma text styles
- [ ] understand frames vs groups, and use auto layout for every new design
- [ ] built at least one component with variants
- [ ] completed Daily UI Days 1-10 in Figma
- [ ] Stark plugin used on at least one design

[Next: Goal 2 - Core UX Skills](02-core.md)
