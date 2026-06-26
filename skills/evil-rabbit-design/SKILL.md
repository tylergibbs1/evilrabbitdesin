---
name: evil-rabbit-design
description: Applies Evil Rabbit's (Vercel's founding brand designer) and the Geist design system's approach when designing, building, or reviewing interfaces, brand, and typography. Use when designing UI, building a marketing or product surface, choosing color/type/spacing, reviewing visual craft, designing a logo or brand mark, deciding whether a flourish earns its place, or matching the Vercel/Geist aesthetic. Triggers on "Vercel style," "Geist," "make it look like Vercel," "monochrome design," "minimal developer-tool aesthetic," "Swiss/grotesque type," "hairline borders," "design system tokens," "is this decorative or functional," "brand mark," "high-contrast minimal UI."
metadata:
  version: 1.0.0
---

# Evil Rabbit Design Principles

Apply how Evil Rabbit (Nicolás Garro Zambrano, founding/principal brand designer at Vercel) and the **Geist** design system he directs think about interfaces, brand, and type. The throughline: **design is a system, not decoration** — constraints are the tool, function outranks flourish, and craft is the manual attention paid to rhythm, structure, and the pixel because it matters, not because someone is checking.

> [!info] Terminology trap
> "Vercel style" in most search results means a surface *aesthetic* — black background, a gradient, a grotesque font, a triangle — that people copy as a look. That is the output, not the method. Copying the look without the system produces a flat imitation. This skill is about the discipline underneath: a tokenized system, monochrome by default, color only when it carries meaning, structure from borders not shadows, and obsessive consistency of rhythm. Apply the method; the look follows.

> [!warning] Sourcing honesty
> Evil Rabbit gives almost no interviews. His genuinely first-person principles come from **one essay he authored** (the Geist Pixel post) plus short posts. The rest is the **Geist system** (his direction, documented at `vercel.com/design`) and third-party characterization. Principles 1–4 below are closest to his own words; 5–10 are the system he shapes. Don't put words in his mouth — see `references/sources.md`.

## When to apply this

Reach for these principles when the task is one of:

- **Designing or reviewing an interface** → use the principles below, then `references/geist-system.md` for exact tokens.
- **Choosing color, type, spacing, radius, motion** → `references/geist-system.md` has the concrete values; don't invent your own scale.
- **Brand, logo, or marketing surface** → `references/visual-language.md` (monochrome foundation, geometry, brand-vs-product split).
- **Judging whether an element earns its place** → "function over gimmick" + "system over novelty" below.
- **Citing or sourcing a claim** → `references/sources.md`, and respect what is/isn't actually attributable to him.

---

## The core principles

### 1. Constraints are the design tool, not a limitation.

Don't treat the system's rules (one type family, a fixed scale, near-monochrome) as walls to work around. They are the instrument that generates the work. *"Constraints weren't a limitation, they were the design tool."* When the palette is tiny and the grid is fixed, every remaining decision — weight, spacing, alignment — has to carry real meaning. Pick the constraints first, then design inside them hard.

### 2. System over novelty. Nothing ships that breaks the rhythm.

A new artifact is judged by whether it can *"adopt without breaking layout or rhythm."* Design is not a sequence of one-off pretty screens; it is one coherent system with predictable metrics and strong cross-layout alignment. Before adding anything, ask: does this share the existing structure, or does it destabilize it? A novelty that breaks the grid is a regression, however striking in isolation.

### 3. Function over gimmick. Design for real production usage.

Make things "as a functional tool within a broader system, not as a visual gimmick." Decoration that doesn't clarify structure, state, or brand intent is noise. Test against real, full, dense, and empty states — not a hero shot. If a flourish only survives in the portfolio screenshot and dies in the product, it failed.

### 4. Craft is manual attention, paid because it matters.

Even on a literal pixel grid, *"each glyph was manually refined to avoid visual noise, uneven weight distribution, and awkward diagonals"* — it "wasn't generated mechanically." Rigor is a habit, not a final pass: consistent metrics, even rhythm, deliberate spacing, hand-tuned alignment. The difference between competent and exceptional is a hundred small decisions nobody asked you to make.

### 5. Monochrome by default. Color must earn its appearance.

The foundation is grayscale, generous whitespace, and hairline borders — and almost nothing else. The "never pure" rule is precise: **text/foreground is always slightly muted** (`#171717` near-black in light, `#ededed` near-white in dark) — never pure `#000`/`#fff` for text — while *backgrounds* can be pure (`#ffffff` light, `#000000` dark; `#fafafa` is the light off-white canvas). **No color for decoration.** Color appears only when it carries meaning: links, focus, status, errors, a single brand accent (**Vercel Blue** — `#006bff` light / `#006efe` dark; legacy `#0070f3`). A grayscale screen with one purposeful accent reads as more confident than a colorful one. Exact scales for both themes in `references/geist-system.md` and `references/geist-spec-dark.md`.

### 6. Structure comes from borders and tonal surfaces, not shadows.

Separate elements with a **1px hairline (`#ebebeb`)** and gentle changes in surface tone. Shadows are deliberately faint and rarely structural. If you reach for a heavy drop shadow to create hierarchy, reach for a border or a tonal step instead. Hierarchy is built from contrast and weight, not from elevation theatrics.

### 7. Typography is the interface. Use Geist (or a Swiss grotesque) with rigor.

Type does most of the design work. Geist is a geometric **Swiss grotesque** with a high x-height, short descenders, and angular terminals — built for crisp rendering at small sizes. Use **Geist Mono** for technical surfaces (code, terminals, diagrams, data, metadata). Set type on the documented scale (`heading-*`, `label-*`, `copy-*`); tighten tracking on large display sizes; let weight and size carry hierarchy before color does. One type family, used precisely, beats a pairing chosen for variety.

### 8. Simplicity, minimalism, speed — strip until only structure remains.

Geist's three stated values. Minimalism here is an engineering stance, not a mood: remove every token that isn't carrying weight. A faster, lighter, quieter interface is the goal, and visual restraint is part of how you get there. If an element doesn't clarify structure, state, or brand, delete it.

### 9. Motion for clarification only — and instant is often best.

Animate to explain a change — never to entertain. Most interactions should feel instant: **`0ms` is frequently the snappiest, best choice.** When motion genuinely helps (revealing or moving an element), keep it short and physical — easing `cubic-bezier(0.175, 0.885, 0.32, 1.1)`, ~150ms for state changes, ~200ms for popovers, ~300ms for overlays/modals. No decorative looping; honor `prefers-reduced-motion`. Stillness is the default; movement is a signal.

### 10. Geometry, grid, and accessibility are non-negotiable.

The grid is a core part of the aesthetic; the brand mark (the upward equilateral triangle / "V") is pure geometry. Align to the grid, pick **one radius family per view** (don't mix rounded and sharp), and respect the spacing rhythm. Keep contrast at **WCAG AA** (4.5:1 body text) and show a visible focus ring on every interactive element at `:focus-visible` — the two-layer ring `0 0 0 2px <surface>, 0 0 0 4px <blue>` (`#006bff` light / `#47a8ff` dark). **Never remove a focus outline without replacing it**, and never signal state with color alone — pair it with an icon or text. High contrast and visible focus are part of the look, not a tax on it.

---

## A working checklist

Copy this when designing or reviewing a surface:

```
Evil Rabbit / Geist review:
- [ ] Did I pick constraints first (type family, scale, palette) and design inside them?
- [ ] Does every element share the system's rhythm, or does something break the grid?
- [ ] Is each flourish functional? Would it survive in the real, dense, production state?
- [ ] Is it grayscale by default? Does any color carry actual meaning, or is it decoration?
- [ ] Is body text muted (#171717 / #ededed, not pure #000/#fff)? Structure from 1px borders, not shadows?
- [ ] Is type doing the hierarchy work? Geist/grotesque, correct scale, ≤2 weights, mono for technical surfaces?
- [ ] On-scale spacing (4px scale), and did I strip every token that isn't carrying weight?
- [ ] Is motion only clarifying a change (often 0ms / ≤300ms) — never decorative?
- [ ] One radius family per view? Aligned to the grid?
- [ ] WCAG AA contrast, visible :focus-visible ring, and state never signaled by color alone?
- [ ] Is the copy precise — verb+noun actions, toasts without "successfully", empty states that point to the next action?
- [ ] Tested against full/empty/long-text states, light and dark?
```

---

## Reference files

- **`references/geist-system.md`** — The distilled, theme-aware token guide: the precise 100–1000 step model, light + dark color anchors, the type scale, the 4px spacing scale, layout column/breakpoints, radius, focus rings, shadows, motion, component defaults, and voice rules. Use this for real values instead of inventing a scale.
- **`references/geist-spec-dark.md`** — The **canonical** machine-readable Geist spec (Dark theme), reproduced verbatim from `vercel.com/design`: every color token (sRGB + P3 `oklch`), the exact typography table, spacing/radius/components, and the full Voice & Content and Do's/Don'ts rules. The source of truth when anything conflicts.
- **`references/visual-language.md`** — The brand and aesthetic layer: monochrome foundation, the triangle's geometry, brand-vs-product color split, his body of work (Vercel rebrand, Geist, Hyper, Now Desktop), and the recurring visual signatures.
- **`references/sources.md`** — Primary sources, what is/isn't attributable to Evil Rabbit personally, and sourcing caveats.
