# Geist system: the concrete tokens

The real Geist design-system values. The principles in `SKILL.md` are the *why*; this is the *what*. There are two themes that share token **names** and differ only in values:

- **Light theme** values are below (primary surfaces white, text near-black).
- **Dark theme** is fully specified in **`geist-spec-dark.md`** — the verbatim machine-readable spec, which is the **source of truth**. When this file and that one disagree, that one wins.

Use these tokens directly instead of inventing a scale. Source: `vercel.com/design`, `vercel.com/geist/colors`.

## Contents
- Color: the step model (precise)
- Color: exact values (light + dark anchors)
- Typography: family and scale
- Spacing and layout
- Border radius
- Borders and shadows
- Focus ring
- Motion
- Component defaults
- Voice & content
- Dark mode and tokens

---

## Color: the step model (precise)

Color is a **10-step semantic scale (100–1000)** across named scales: `background`, `gray`, `gray-alpha`, `blue`, `red`, `amber`, `green`, `teal`, `purple`, `pink`. The step encodes **intent, not just lightness** — this exact mapping is load-bearing:

| Step | Role |
|---|---|
| 100 | default background |
| 200 | hover background |
| 300 | active background |
| 400 | default border |
| 500 | hover border |
| 600 | active border |
| 700 | solid fill, high contrast |
| 800 | solid fill, hover |
| 900 | secondary text & icons |
| 1000 | primary text & icons |

So within any scale: 100/200/300 are background/hover/active, 400/500/600 are border/hover/active, 700/800 are solid fills, 900/1000 are text. State transitions step up the scale (a 100 fill → 200 on hover → 300 on active; a 400 border → 500 → 600).

**Accent meaning:** `blue` = success, links, and focus · `red` = errors · `amber` = warnings · plus `green`, `teal`, `purple`, `pink`. P3/wide-gamut (`*-p3`, in `oklch()`) renders on supported displays; sRGB hex is the fallback.

## Color: exact values (light + dark anchors)

**Light theme (primary surfaces light):**
- Primary text / fill: **`#171717`** (`gray-1000` — near-black, **never pure `#000`** for text)
- Secondary text: **`#4d4d4d`**
- Background base: **`#ffffff`** (`background-100`); off-white canvas: **`#fafafa`** (`background-200`)
- Hairline border: **`#ebebeb`** (the `#eaeaea` in his older code is the same family)
- Gray scale: `gray-100 #f2f2f2` → … → `gray-1000 #171717`
- Accent — Vercel Blue `blue-700`: **`#006bff`** (legacy "Vercel Blue" **`#0070f3`** still recognized)

**Dark theme anchors** (full set in `geist-spec-dark.md`):
- Primary text: **`#ededed`** (`gray-1000` — near-white, **not pure `#fff`**); secondary `#a0a0a0`
- Background base: **`#000000`** (`background-100` — pure black *is* used as the dark surface)
- Accent `blue-700`: **`#006efe`**; focus ring uses `blue-900` **`#47a8ff`**
- `gray-alpha-*` are translucent whites (`#ffffff12` … `#ffffffeb`) for borders/overlays/hover

**The accurate "never pure" rule:** *text/foreground* is always slightly muted (`#171717` light, `#ededed` dark), while *backgrounds* can be pure `#000`/`#fff`. Don't set body text to pure black or pure white.

> Reminder from principle 5: accents exist for **meaning** (status, links, focus, brand), not decoration. A correct Geist screen is mostly gray with one purposeful accent.

## Typography: family and scale

**Family:** Geist Sans (UI + prose) + Geist Mono (code, data, tabular figures); Geist Pixel for bitmap/display. A geometric **Swiss grotesque** — high x-height, short descenders, angular terminals, tuned for small-size rendering. 9 weights (Thin → UltraBlack). SIL OFL 1.1. Free fallback: Inter.

**Use Geist Mono** for code, terminals, diagrams, tables of numbers, IDs, timestamps, metadata — the `-mono` type tokens (`copy-14-mono`, `label-13-mono`, etc.) pair it with the same metrics. Prefer tabular figures when numbers must align.

**Token families** (each preset bundles size + line-height + weight + letter-spacing — full table with exact values in `geist-spec-dark.md`):
- `heading-72 … heading-14` — headings, weight 600; **letter-spacing tightens hard as size grows** (e.g. heading-72 = 72px/-4.32px, heading-24 = 24px/-0.96px).
- `label-20 … label-12` — single-line scannable text (nav, form labels, table headers, metadata), weight 400.
- `copy-24 … copy-13` — multi-line body, weight 400, taller line-height.
- `button-16 … button-12` — medium weight (500) control labels.

Default body ≈ `copy-14` / `label-14`. Let **size and weight** carry hierarchy before color does, and **don't use more than two font weights in one view.**

## Spacing and layout

**Spacing scale (4px base), with token indices:** `1:4 · 2:8 · 3:12 · 4:16 · 6:24 · 8:32 · 10:40 · 16:64 · 24:96` (px). Off-scale values (7px, 13px, 22px) are the most common way a layout quietly loses the Geist feel.

**Rhythm:** 8px inside a group · 16px between groups · 32–40px between sections.

**Layout:** center content in a **1200px max column** with side padding that grows at wider breakpoints; every layout works mobile + desktop. Card padding: **24px** default, **16px** compact, **32px** hero. Breakpoints: `sm` 401 · `md` 601 · `lg` 961 · `xl` 1200 · `2xl` 1400 (px).

## Border radius

| Token | Value | Use |
|---|---|---|
| `sm` | **6px** | Everyday surfaces — buttons, inputs, cards |
| `md` | **12px** | Menus, modals, popovers |
| `lg` | **16px** | Fullscreen / large surfaces |
| `full` | **9999px** | Pills, avatars, circular controls |

Rule: **one radius family per view.** Don't mix rounded and sharp.

## Borders and shadows

Borders and tonal surfaces do the structural work; shadows stay subtle. Light-theme reference shadows:
- Card: `0 2px 2px rgba(0,0,0,0.04)`
- Popover: `0 1px 1px rgba(0,0,0,0.02), 0 4px 8px -4px rgba(0,0,0,0.04), 0 16px 24px -8px rgba(0,0,0,0.06)`
- Modal: `0 1px 1px rgba(0,0,0,0.02), 0 8px 16px -4px rgba(0,0,0,0.04), 0 24px 32px -8px rgba(0,0,0,0.06)`

(Dark-theme shadows differ — raised card is `0 1px 2px rgba(0,0,0,0.16)`; see `geist-spec-dark.md`.) If you're using a shadow to create hierarchy, reach for a border or a tonal step instead.

## Focus ring

A two-layer ring: a 2px gap in the surface color, then a 2px blue ring. Shown on every interactive element at `:focus-visible`.

```css
/* Light theme */ box-shadow: 0 0 0 2px #ffffff, 0 0 0 4px #006bff;
/* Dark theme  */ box-shadow: 0 0 0 2px #000000, 0 0 0 4px #47a8ff;  /* blue-900 */
```

Never remove a focus outline without an equally visible replacement.

## Motion

- **Purpose:** clarification only — explain a state change or preserve spatial continuity. Never decorative.
- **Often the best duration is `0ms`** — most interactions should feel instant. Only animate when motion genuinely helps.
- When it does: short and physical, easing **`cubic-bezier(0.175, 0.885, 0.32, 1.1)`** — ~150ms state changes, ~200ms popovers/tooltips, ~300ms overlays/modals.
- No looping or attention-grabbing animation. Honor `prefers-reduced-motion`.

## Component defaults

(Medium = 40px is the default size; small = 32px, large = 48px steps up to `button-16`.)

- **Primary button:** `gray-1000` fill, `background-100` text, **40px** height, **6px** radius, padding `0 10px`.
- **Secondary button:** `background-100` fill + translucent (`gray-alpha-400`) border.
- **Tertiary button:** transparent, `gray-1000` text; tints with `gray-alpha` on hover.
- **Error button:** `red-800` fill, white text — destructive actions.
- **Input:** `background-100` fill, translucent border, **40px** height, **6px** radius, padding `0 12px`.
- **Disabled:** `gray-100` fill, `gray-700` text, not-allowed cursor.

Geist components are published as `@vercel/geistcn`. When building React UI that should match, prefer pulling the real components/tokens over re-deriving them.

## Voice & content

Copy is part of the design (full rules in `geist-spec-dark.md`): **Title Case** for labels/buttons/titles/tabs, **sentence case** for body/helper/toasts; actions are **verb + noun** (`Deploy Project`, never `OK`/`Confirm`); errors state what happened + what to do next; toasts drop the trailing period and **never say "successfully"** (`Project deleted`); empty states point to the first action; in-progress uses present participle + ellipsis (`Deploying…`).

## Dark mode and tokens

Scales are semantic CSS variables (`var(--ds-gray-1000)`, `var(--ds-background-100)`, etc.), so light/dark swap by token, not by rewriting hex. `gray-alpha-*` exists so overlays survive a theme switch. Design against tokens when a surface must theme; reserve raw hex for one-off brand/marketing work.

---

## Unverified — do not cite as fact

- A "**1440 units-per-em** font grid" is sometimes repeated for Geist but is **not confirmed** by any primary source (the 16px figure is a CSS/system base, not a font-design grid). Don't state it as fact.
- "Simplicity, minimalism, speed" is the **font** framing (`vercel.com/font`); the system docs emphasize **consistency** and a **high-contrast, accessible** color system. Attribute each precisely.
