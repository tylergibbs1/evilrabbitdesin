# Visual language: the brand and aesthetic layer

The `geist-system.md` file is the *what* (tokens). This is the *feel*: the brand foundation, the geometry, and the body of work that made the Vercel/Evil Rabbit aesthetic recognizable. Use this when designing brand, marketing, or logo work — or when someone says "make it feel like Vercel" and you need to know what that actually means beyond a black background.

## Contents
- The monochrome foundation
- Brand vs. product color
- Geometry and the triangle
- Recurring visual signatures
- The body of work
- What makes an imitation flat

---

## The monochrome foundation

The brand is built on **black, white, Geist, and almost nothing else.** The precise discipline (it's about *text*, not surfaces):

- **Text/foreground is muted, never pure:** near-black **`#171717`** in light, near-white **`#ededed`** in dark. Pure `#000`/`#fff` *text* reads as harsh and unconsidered.
- **Backgrounds can be pure:** white **`#ffffff`** (light) or black **`#000000`** (dark); **`#fafafa`** is the light off-white canvas.
- Hairline borders **`#ebebeb`** (light) / translucent white `gray-alpha` (dark).

The discipline that makes it work: **no color for decoration.** A marketing page is mostly black/white/gray with generous whitespace, real product UI or abstract geometry as the only imagery, and color introduced *only* where it carries meaning. Restraint reads as confidence; a colorful developer-tool page reads as trying too hard.

## Brand vs. product color

There are two registers, and conflating them is a common mistake:

- **Brand / marketing** is near-monochrome and high-contrast. Color is rare and intentional.
- **Product (Geist UI)** adds the functional accent scales (blue, red, amber, green, teal, purple, pink) — but strictly for **semantic state**: a green success, a red error, a blue link or primary action. Grays still dominate the screen.

So "Vercel uses color" and "Vercel is monochrome" are both true at different layers. When in doubt, default toward monochrome and justify every accent.

## Geometry and the triangle

The Vercel mark is an **upward-pointing equilateral triangle** (echoing the "V"), rendered as a black triangle on white, or inverted to a white triangle inside a solid black roundel for the icon. It is pure geometry — no gradient, no ornament, no wordmark dependency.

The grid is described as a core part of the aesthetic. Layouts align to it; the triangle's equilateral precision is the same instinct applied to a logo. When designing marks or layouts in this language: start from geometric primitives, keep them exact, and resist decorating them.

## Recurring visual signatures

Patterns that show up across his work and the Vercel surface (some documented, some observed from his own code — see `sources.md`):

- **Hairline `#eaeaea`/`#ebebeb` borders** dividing content into clean cells, instead of cards floating on shadows.
- **Subtle `#fafafa`/`#FAFBFC` tonal fills** to separate regions without adding a border or a color.
- **A single blue link/accent** (`#0070f3` historically, `#006bff` now) against otherwise monochrome text.
- **Muted gray secondary text** (`#999`, `#4d4d4d`) for metadata, dates, and chrome that should recede.
- **Large, thin display headings** (light weights at big sizes) with tight tracking, paired with small precise body text.
- **Backdrop blur on sticky chrome** (`backdrop-filter: blur(8px)` over a translucent white) so navigation recedes without a hard edge.
- **Generous whitespace and a constrained max-width** (~980px content column in his portfolio) — density where it matters, air around it.

## The body of work

Useful for grounding the aesthetic in real artifacts (from his portfolio at evilrabb.it and public record):

- **Vercel brand & website** — the rebrand from ZEIT to Vercel (2020); the marketing site that defined the "monochrome developer-tool" look many now imitate. Award-winning (CSSDA, 2019-era ZEIT site).
- **Geist** (2023) — the typeface and design system. Directed by Evil Rabbit; the font itself was built with basement.studio (designers Andrés Briganti, Mateo Zaragoza; font developer Guido Ferreyra). Geist Mono shipped as the technical companion. **Geist is a team effort he directed, not a solo draw** — don't overstate sole authorship.
- **Geist Pixel** — a later bitmap/pixel companion font; the one artifact he wrote about first-person, framing it as a *system extension*, not a novelty.
- **Hyper** — the Electron-based terminal (hyper.is); minimal, themeable, monospaced.
- **Now Desktop** — the ZEIT/Now desktop app, featured on Electron's front page alongside VS Code, Figma, Slack.
- **Next.js Conf** branding and launch visuals (collaborations with basement.studio).

## What makes an imitation flat

The aesthetic is widely cloned and usually badly. The tells of a shallow copy, and the fix:

| Shallow imitation | The actual discipline |
|---|---|
| Pure `#000` background | Near-black `#171717`; black is reserved and considered |
| Color used decoratively because "Vercel uses blue" | Color only for meaning; mostly monochrome |
| Heavy drop shadows for hierarchy | 1px hairline borders + tonal surfaces |
| A grotesque font chosen, then ignored | Type on a strict scale, tight display tracking, mono for technical surfaces |
| Off-grid spacing (7px, 13px) | The 4px scale, consistent rhythm |
| Decorative motion / looping gradients | Motion only to clarify, ≤300ms |
| One pretty hero screen | Every state designed — full, empty, long-text, dark |

The look is downstream of the system. Build the system and the look is unavoidable; chase the look and you get the flat version.
