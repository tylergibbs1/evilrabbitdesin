# Geist — official machine-readable spec (Dark theme)

This is Vercel's canonical Geist design-system spec, **Dark theme**, reproduced verbatim from `vercel.com/design` (the `version: alpha` token document). The Light theme uses the same token *names* with different values and is at `vercel.com/design.md`. This is the source of truth — when `geist-system.md`'s distilled guidance and this file disagree, **this file wins**. Use the exact token values below rather than approximating.

```yaml
version: alpha
name: Geist
description: Vercel's Geist design system, Dark theme (the Light theme is documented at /design.md).
colors:
  primary: "#ededed"        # gray-1000 — primary text/icons
  secondary: "#a0a0a0"      # gray-900 — secondary text/icons
  tertiary: "#006efe"       # blue-700 — accent (links, focus, primary state)
  neutral: "#1a1a1a"        # gray-100
  background-100: "#000000" # primary page/card surface (pure black in dark)
  background-200: "#000000" # secondary surface (subtle separation only)
  gray-100: "#1a1a1a"
  gray-200: "#1f1f1f"
  gray-300: "#292929"
  gray-400: "#2e2e2e"
  gray-500: "#454545"
  gray-600: "#878787"
  gray-700: "#8f8f8f"
  gray-800: "#7d7d7d"
  gray-900: "#a0a0a0"
  gray-1000: "#ededed"
  gray-alpha-100: "#ffffff12"
  gray-alpha-200: "#ffffff17"
  gray-alpha-300: "#ffffff21"
  gray-alpha-400: "#ffffff24"
  gray-alpha-500: "#ffffff3d"
  gray-alpha-600: "#ffffff82"
  gray-alpha-700: "#ffffff8a"
  gray-alpha-800: "#ffffff78"
  gray-alpha-900: "#ffffff9c"
  gray-alpha-1000: "#ffffffeb"
  blue-100: "#06193a"
  blue-200: "#022248"
  blue-300: "#002f62"
  blue-400: "#003674"
  blue-500: "#00418b"
  blue-600: "#0090ff"
  blue-700: "#006efe"
  blue-800: "#005be7"
  blue-900: "#47a8ff"
  blue-1000: "#eaf6ff"
  red-100: "#330a11"
  red-200: "#440d13"
  red-300: "#5d0e17"
  red-400: "#6f101b"
  red-500: "#88151f"
  red-600: "#f32e40"
  red-700: "#f13242"
  red-800: "#e2162a"
  red-900: "#ff565f"
  red-1000: "#ffe9ed"
  amber-100: "#2a1700"
  amber-200: "#361900"
  amber-300: "#502800"
  amber-400: "#5b3000"
  amber-500: "#703e00"
  amber-600: "#ed9a00"
  amber-700: "#ffae00"
  amber-800: "#ff9300"
  amber-900: "#ff9300"
  amber-1000: "#fff3d5"
  green-100: "#002608"
  green-200: "#00320b"
  green-300: "#003a0e"
  green-400: "#004615"
  green-500: "#006717"
  green-600: "#00952d"
  green-700: "#00ac3a"
  green-800: "#009432"
  green-900: "#00ca50"
  green-1000: "#d8ffe4"
  teal-100: "#00231b"
  teal-200: "#002b22"
  teal-300: "#003d34"
  teal-400: "#004035"
  teal-500: "#006354"
  teal-600: "#009e86"
  teal-700: "#00aa95"
  teal-800: "#00927f"
  teal-900: "#00cfb7"
  teal-1000: "#cbfff5"
  purple-100: "#290c33"
  purple-200: "#341142"
  purple-300: "#47185e"
  purple-400: "#541a76"
  purple-500: "#642290"
  purple-600: "#9440d5"
  purple-700: "#9440d5"
  purple-800: "#7d2bba"
  purple-900: "#c472fb"
  purple-1000: "#fbecff"
  pink-100: "#310d1e"
  pink-200: "#420c25"
  pink-300: "#571032"
  pink-400: "#5d0c34"
  pink-500: "#76063f"
  pink-600: "#ba0056"
  pink-700: "#f12b82"
  pink-800: "#e7006d"
  pink-900: "#ff4d8d"
  pink-1000: "#ffe9f4"
  # Wide-gamut accent variants in oklch for P3 displays (sRGB hex above is the fallback)
  blue-100-p3: "oklch(22.17% 0.069 259.89)"
  blue-200-p3: "oklch(25.45% 0.0811 255.8)"
  blue-300-p3: "oklch(30.86% 0.1022 255.21)"
  blue-400-p3: "oklch(34.1% 0.121 254.74)"
  blue-500-p3: "oklch(38.5% 0.1403 254.4)"
  blue-600-p3: "oklch(64.94% 0.1982 251.8131841760864)"
  blue-700-p3: "oklch(57.61% 0.2321 258.23)"
  blue-800-p3: "oklch(51.51% 0.2307 257.85)"
  blue-900-p3: "oklch(71.7% 0.1648 250.79360374054167)"
  blue-1000-p3: "oklch(96.75% 0.0179 242.4234217368056)"
  red-100-p3: "oklch(22.1% 0.0657 15.11)"
  red-200-p3: "oklch(25.93% 0.0834 19.02)"
  red-300-p3: "oklch(31.47% 0.1105 20.96)"
  red-400-p3: "oklch(35.27% 0.1273 21.23)"
  red-500-p3: "oklch(40.68% 0.1479 23.16)"
  red-600-p3: "oklch(62.56% 0.2277 23.03)"
  red-700-p3: "oklch(62.56% 0.2234 23.03)"
  red-800-p3: "oklch(58.01% 0.227 25.12)"
  red-900-p3: "oklch(69.96% 0.2136 22.03)"
  red-1000-p3: "oklch(95.6% 0.0293 6.61)"
  amber-100-p3: "oklch(22.46% 0.0538 76.04)"
  amber-200-p3: "oklch(24.95% 0.0642 64.78)"
  amber-300-p3: "oklch(32.34% 0.0837 63.83)"
  amber-400-p3: "oklch(35.53% 0.0903 66.29707162673735)"
  amber-500-p3: "oklch(41.55% 0.1044 67.98)"
  amber-600-p3: "oklch(75.04% 0.1737 74.49)"
  amber-700-p3: "oklch(81.87% 0.1969 76.46)"
  amber-800-p3: "oklch(77.21% 0.1991 64.28)"
  amber-900-p3: "oklch(77.21% 0.1991 64.28)"
  amber-1000-p3: "oklch(96.7% 0.0418 84.59)"
  green-100-p3: "oklch(23.09% 0.0716 149.68)"
  green-200-p3: "oklch(27.12% 0.0895 150.09)"
  green-300-p3: "oklch(29.84% 0.096 149.25)"
  green-400-p3: "oklch(34.39% 0.1039 147.78)"
  green-500-p3: "oklch(44.19% 0.1484 147.2)"
  green-600-p3: "oklch(58.11% 0.1815 146.55)"
  green-700-p3: "oklch(64.58% 0.199 147.27)"
  green-800-p3: "oklch(57.81% 0.1776 147.5)"
  green-900-p3: "oklch(73.1% 0.2158 148.29)"
  green-1000-p3: "oklch(96.76% 0.056 154.18)"
  teal-100-p3: "oklch(22.1% 0.0544 178.74)"
  teal-200-p3: "oklch(25.06% 0.062 178.76)"
  teal-300-p3: "oklch(31.5% 0.0767 180.99)"
  teal-400-p3: "oklch(32.43% 0.0763 180.13)"
  teal-500-p3: "oklch(43.35% 0.1055 180.97)"
  teal-600-p3: "oklch(60.71% 0.1485 180.24)"
  teal-700-p3: "oklch(64.92% 0.1403 181.95)"
  teal-800-p3: "oklch(57.53% 0.1392 181.66)"
  teal-900-p3: "oklch(74.56% 0.1765 182.8)"
  teal-1000-p3: "oklch(96.46% 0.056 180.29)"
  purple-100-p3: "oklch(22.34% 0.0779 316.87)"
  purple-200-p3: "oklch(25.91% 0.0921 314.41)"
  purple-300-p3: "oklch(31.98% 0.1219 312.41)"
  purple-400-p3: "oklch(35.93% 0.1504 309.78)"
  purple-500-p3: "oklch(40.99% 0.1721 307.92)"
  purple-600-p3: "oklch(55.5% 0.2191 306.12)"
  purple-700-p3: "oklch(55.5% 0.2186 306.12)"
  purple-800-p3: "oklch(48.58% 0.2102 305.73)"
  purple-900-p3: "oklch(69.87% 0.2037 309.51)"
  purple-1000-p3: "oklch(96.1% 0.0304 316.46)"
  pink-100-p3: "oklch(22.67% 0.0628 354.73)"
  pink-200-p3: "oklch(26.2% 0.0859 356.68)"
  pink-300-p3: "oklch(31.15% 0.1067 355.93)"
  pink-400-p3: "oklch(32.13% 0.1174 356.71)"
  pink-500-p3: "oklch(37.01% 0.1453 358.39)"
  pink-600-p3: "oklch(50.33% 0.2089 4.33)"
  pink-700-p3: "oklch(63.52% 0.2346 1.01)"
  pink-800-p3: "oklch(59.51% 0.2429 4.21)"
  pink-900-p3: "oklch(69.36% 0.2223 3.91)"
  pink-1000-p3: "oklch(95.74% 0.0326 350.08)"
```

## Typography tokens (exact)

Each token carries `fontFamily` / `fontSize` / `fontWeight` / `lineHeight` / `letterSpacing`. `letterSpacing` is only set on headings (it tightens as size grows) and is absent (default) on label/copy/button.

| Token | Family | Size | Weight | Line height | Letter-spacing |
|---|---|---|---|---|---|
| heading-72 | Geist Sans | 72px | 600 | 72px | -4.32px |
| heading-64 | Geist Sans | 64px | 600 | 64px | -3.84px |
| heading-56 | Geist Sans | 56px | 600 | 56px | -3.36px |
| heading-48 | Geist Sans | 48px | 600 | 56px | -2.88px |
| heading-40 | Geist Sans | 40px | 600 | 48px | -2.4px |
| heading-32 | Geist Sans | 32px | 600 | 40px | -1.28px |
| heading-24 | Geist Sans | 24px | 600 | 32px | -0.96px |
| heading-20 | Geist Sans | 20px | 600 | 26px | -0.4px |
| heading-16 | Geist Sans | 16px | 600 | 24px | -0.32px |
| heading-14 | Geist Sans | 14px | 600 | 20px | -0.28px |
| button-16 | Geist Sans | 16px | 500 | 20px | — |
| button-14 | Geist Sans | 14px | 500 | 20px | — |
| button-12 | Geist Sans | 12px | 500 | 16px | — |
| label-20 | Geist Sans | 20px | 400 | 32px | — |
| label-18 | Geist Sans | 18px | 400 | 20px | — |
| label-16 | Geist Sans | 16px | 400 | 20px | — |
| label-14 | Geist Sans | 14px | 400 | 20px | — |
| label-14-mono | Geist Mono | 14px | 400 | 20px | — |
| label-13 | Geist Sans | 13px | 400 | 16px | — |
| label-13-mono | Geist Mono | 13px | 400 | 20px | — |
| label-12 | Geist Sans | 12px | 400 | 16px | — |
| label-12-mono | Geist Mono | 12px | 400 | 16px | — |
| copy-24 | Geist Sans | 24px | 400 | 36px | — |
| copy-20 | Geist Sans | 20px | 400 | 36px | — |
| copy-18 | Geist Sans | 18px | 400 | 28px | — |
| copy-16 | Geist Sans | 16px | 400 | 24px | — |
| copy-14 | Geist Sans | 14px | 400 | 20px | — |
| copy-14-mono | Geist Mono | 14px | 400 | 20px | — |
| copy-13 | Geist Sans | 13px | 400 | 18px | — |
| copy-13-mono | Geist Mono | 13px | 400 | 18px | — |

## Spacing, radius, components

```yaml
spacing:   # 4px base
  1: 4px ·  2: 8px ·  3: 12px ·  4: 16px ·  6: 24px ·  8: 32px ·  10: 40px ·  16: 64px ·  24: 96px
rounded:
  sm: 6px ·  md: 12px ·  lg: 16px ·  full: 9999px
components:
  button-primary:   bg {primary} · text {background-100} · {button-14} · {sm} · padding 0 10px · height 40px
  button-secondary: bg {background-100} · text {primary} · {button-14} · {sm} · padding 0 10px · height 40px
  button-tertiary:  text {primary} · {button-14} · {sm} · padding 0 10px · height 40px
  button-error:     bg {red-800} · text #ffffff · {button-14} · {sm} · padding 0 10px · height 40px
  button-small:     {button-14} · {sm} · padding 0 6px · height 32px
  button-large:     {button-16} · {sm} · padding 0 14px · height 48px
  input:            bg {background-100} · text {primary} · {label-14} · {sm} · padding 0 12px · height 40px
  input-small:      {label-14} · {sm} · padding 0 12px · height 32px
  input-large:      {label-16} · {sm} · padding 0 12px · height 48px
```

## Step semantics (the precise model — load-bearing)

Each non-background scale runs 10 steps, and the step encodes **intent, not just lightness**:

| Step | Meaning |
|---|---|
| 100 | default background |
| 200 | hover background |
| 300 | active background |
| 400 | default border |
| 500 | hover border |
| 600 | active border |
| 700 | solid fill, high contrast |
| 800 | solid fill, hover |
| 900 | secondary text and icons |
| 1000 | primary text and icons |

- `background-100` = primary page/card surface; `background-200` = secondary surface for subtle separation only (don't use as a general fill).
- `gray-alpha-*` are translucent — use for borders, dividers, overlays, hover. Solid `gray-*` holds contrast on any surface — use for text and opaque fills. They are **separate scales from `background-*`; don't swap them.**
- Accent meaning: **`blue` = success, links, and focus; `red` = errors; `amber` = warnings;** plus `green`, `teal`, `purple`, `pink`.
- State progression: a `100` fill → `200` hover → `300` active; a `400` border → `500` → `600`. Disabled = `gray-100` fill, `gray-700` text, not-allowed cursor.

## Layout

- Spacing rhythm: **8px inside a group, 16px between groups, 32–40px between sections.**
- Card padding: **24px** default, **16px** compact, **32px** hero.
- Content column: **centered, 1200px max**, side padding grows at wider breakpoints. Every layout works mobile + desktop.
- Breakpoints: `sm` 401px · `md` 601px · `lg` 961px · `xl` 1200px · `2xl` 1400px.

## Elevation (Dark theme box-shadows)

Hierarchy comes from tonal surfaces and borders first; shadows stay subtle.

- Raised cards: `0 1px 2px rgba(0,0,0,0.16)`
- Popovers/menus: `0 1px 1px rgba(0,0,0,0.02), 0 4px 8px -4px rgba(0,0,0,0.04), 0 16px 24px -8px rgba(0,0,0,0.06)`
- Modals/dialogs: `0 1px 1px rgba(0,0,0,0.02), 0 8px 16px -4px rgba(0,0,0,0.04), 0 24px 32px -8px rgba(0,0,0,0.06)`
- Tooltips: the lightest of these. Pair each elevation with the matching radius.

## Motion

- Use motion only when it clarifies a change. **Most interactions should feel instant — `0ms` is often the snappiest, best choice** (context-dependent).
- When motion helps (revealing/moving an element): short and physical, easing **`cubic-bezier(0.175, 0.885, 0.32, 1.1)`** — ~150ms state changes, ~200ms popovers/tooltips, ~300ms overlays/modals.
- No long, looping, or attention-grabbing animation. Honor `prefers-reduced-motion` (drop nonessential motion).

## Focus ring (Dark theme)

Two-layer ring: a 2px gap in the surface color, then a 2px `blue-900` ring.

```css
box-shadow: 0 0 0 2px #000000, 0 0 0 4px #47a8ff;
```

Show it on every interactive element at `:focus-visible`. Never remove an outline without a visible replacement. (Light theme uses the same pattern with the light surface color + its blue.)

## Voice & content

Copy is part of the design — precise, no filler.

- **Title Case** for labels, buttons, titles, tabs; **sentence case** for body, helper text, toasts.
- Actions = **verb + noun** (`Deploy Project`, `Delete Member`) — never `Confirm`, `OK`, or a bare verb.
- Errors = what happened + what to do next: `Build failed. Bundle exceeds 50 MB. Reduce it or raise the limit.`
- Toasts name the specific thing changed, **drop the trailing period, never say "successfully"**: `Project deleted`, not `Successfully deleted the project.`
- Empty states point to the first action: `No deployments yet. Push to your Git repository to create one.`
- In-progress = present participle + ellipsis: `Deploying…`, `Saving…`.
- Numerals (`3 projects`), curly quotes, real ellipsis character. Skip `please` and marketing superlatives.

## Do's and don'ts

- Use the gray scale to rank info: `1000` primary text, `900` secondary, `700` disabled.
- Keep solid accent color for state and the single most important action on a view.
- Hold **WCAG AA** contrast (4.5:1 body text).
- Show the focus ring on every interactive element at `:focus-visible`.
- Apply typography tokens instead of hand-setting size/line-height/weight.
- Don't signal state with **color alone** — pair with an icon or text label.
- Don't use `background-200` as a general fill (subtle separation only).
- Don't mix rounded and sharp corners, or more than two font weights, in one view.
- Don't swap `gray-*` for `background-*` — separate scales.
