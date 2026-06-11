# 🎨 Phase 1: Foundations

> **~130 hrs total** · your pace, no deadline
> Visual design principles, color theory, typography, and Figma fundamentals. This is the visual grammar everything else depends on.

[← Phase 0](00-prep.md) · [Hub](README.md) · [Next: Phase 2 — Core UX Skills →](02-core.md)

---

## Visual Design Principles (~40 hrs)

Visual design is a language with rules. Worth learning them before you break them.

### What to cover

- **Hierarchy:** the eye reads in order. Size, weight, contrast, and position direct attention. Every layout decision is a hierarchy decision.
- **Contrast:** the difference between elements — lightness, color, size, shape — creates emphasis and guides the eye. Low contrast is the most common beginner mistake.
- **Alignment:** invisible grid lines hold a layout together. Misalignment reads as carelessness.
- **Proximity:** related elements belong together; unrelated elements belong apart. Proximity communicates grouping before any text does.
- **White space:** "negative space" isn't wasted space. It reduces cognitive load and increases perceived quality.
- **Repetition:** consistent visual patterns create unity. Design systems are formalized repetition.
- **Scale and proportion:** size relationships between elements — headings, body copy, buttons, icons — communicate importance hierarchy.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [Sharpen.design](https://sharpen.design) | Web | Generate random UI design prompts — apply each principle deliberately | **Free** |
| Figma fundamentals (in-app tutorial) | Figma | Complete the official "Figma for beginners" 4-part tutorial to learn the tool and apply layout principles | **Free** |
| [DesignCourse on YouTube](https://www.youtube.com/@DesignCourse) | YouTube | Watch the "UI Design Fundamentals" series and recreate 3 examples in Figma | **Free** |
| [Refactoring UI — free chapter](https://www.refactoringui.com) | Web | Read the free preview; apply the hierarchy and spacing techniques to a blank card component | **Free** |

**Practice gate:** you can look at any UI, spot at least 3 hierarchy or layout problems, and explain *why* they're problems before moving on.

---

## Color Theory & Typography (~40 hrs)

Two foundational systems that carry most of a design's emotional weight and readability.

### Color theory

- **Color models:** HSL (hue, saturation, lightness) is how you think about color in UI; RGB and hex are how you implement it.
- **Color wheel basics:** complementary, analogous, triadic schemes — and why "complementary" often works better as an accent than a 50/50 split.
- **Saturation and lightness:** most beginner color mistakes come down to over-saturation. Professional palettes use muted, shifted tones, not pure hues.
- **Semantic color:** in UI, color carries meaning (red = error/destructive, green = success). Consistency is a usability feature, not decoration.
- **Accessibility:** color alone must never be the only visual signal. WCAG 2.2 minimum contrast ratios: 4.5:1 for normal text, 3:1 for large text and UI components.
- **Building a palette:** one neutral scale + one brand color + two semantic colors (success/error) covers most UI needs.

### Typography

- **Type anatomy:** baseline, x-height, ascenders, descenders, kerning, tracking, leading. These are the vocabulary for precise type control.
- **Type scale:** modular scales (e.g., 1.25 or 1.333 ratio) create consistent heading/body size relationships.
- **Font pairing:** one display/heading font + one body font is the safe default. More than two families usually reads as noise.
- **Variable fonts:** useful for reducing load in web UI; worth knowing they exist.
- **Readability rules of thumb:** body copy 15–20px, line-height 1.4–1.6, line length 60–75 characters for comfortable reading.
- **Choosing typefaces:** system fonts (Inter, SF Pro, Roboto) are workhorses. Use free Google Fonts for early projects; don't worry about licensing until you're designing for a real client.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [Coolors.co](https://coolors.co) | Web | Generate 5 accessible UI color palettes and check each against WebAIM Contrast Checker | **Free** |
| [Google Fonts](https://fonts.google.com) | Web | Build a type specimen in Figma: heading, subheading, body, caption with a modular scale | **Free** |
| [Typescale.com](https://typescale.com) | Web | Experiment with 3 different ratios and export a scale you'll use in your Phase 4 case study | **Free** |
| Figma color styles exercise | Figma | Create a local color style library: neutral scale + brand color + success/error/warning semantic tokens | **Free** |

> Color and accessibility aren't separate concerns — build accessible color into your mental model now, not as a retrofit step. Use the Stark Figma plugin every time you make a color decision.

**Practice gate:** you can build a 5-color accessible UI palette from scratch, verify all text/background combinations meet WCAG 2.2 AA (4.5:1), and explain *why* each color was chosen before moving on.

---

## Figma Fundamentals (~50 hrs)

Figma is the industry-default design and prototyping tool. Learn it deeply.

### What to cover

- **Frames vs groups:** frames are the building block of Figma layouts; groups are for quick organization. Know when to use each.
- **Auto layout:** Figma's flexbox-like system for responsive, resizable components. This is the single most important Figma skill after drawing. Resize behavior (fill/hug/fixed) is where most beginners get stuck.
- **Components and variants:** a button with states (default, hover, disabled) should be one component with variants, not four separate frames. Component properties (text, boolean, instance swap) reduce duplication.
- **Styles and variables:** text styles, color styles, effect styles, and (in newer Figma) variables for design tokens. This is how you build the foundation of a design system.
- **Prototyping:** linking frames with interactions. Know the difference between instant, dissolve, and smart-animate transitions and when each feels right.
- **Dev Mode:** basic familiarity — how a developer reads your Figma file, what measurements and tokens they see.
- **Plugins:** Stark (accessibility), Unsplash (free images), Iconify (icons). Keep the plugin list short early on.

> **Figma pricing reality:** The free Starter tier is 1 team, 3 Figma files, unlimited FigJam. When your 3-file limit becomes a problem, archive old projects or use Penpot for overflow work. You don't need Pro for learning.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [Figma "Explore design" tutorials](https://www.figma.com/resources/learn-design/) | Figma | Complete the "Components," "Auto layout," and "Prototyping" modules and publish a component set to a community file | **Free** |
| [Figma Community](https://www.figma.com/community) | Figma | Find a mobile app UI kit, duplicate it, and redesign one screen using its own component library | **Free** |
| [Jesse Showalter on YouTube](https://www.youtube.com/@JesseShowalter) | YouTube | Watch the Figma auto-layout deep-dive; rebuild the example from scratch | **Free** |
| [Daily UI](https://www.dailyui.co) | Web (email) | Sign up — complete Days 1–10. Design each prompt as a Figma frame with real auto layout and components | **Free** |

**Practice gate:** you can build a mobile app screen with auto layout, a component button with 3 variants, and a working prototype flow (at least 3 linked screens) before moving on.

---

## Phase 1 exit checklist

- [ ] Can identify hierarchy, contrast, alignment, and proximity issues in any UI
- [ ] Built a 5-color accessible palette with verified contrast ratios
- [ ] Built a type scale (heading → body → caption) as Figma text styles
- [ ] Understand frames vs groups, and use auto layout for every new design
- [ ] Built at least one component with variants
- [ ] Completed Daily UI Days 1–10 in Figma
- [ ] Stark plugin used on at least one design

Next: [Phase 2 — Core UX Skills (Research, IA, Wireframing, Accessibility, Design Systems) →](02-core.md)
