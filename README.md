# Evil Rabbit Design

How Evil Rabbit (Vercel's founding brand designer) and the **Geist** design system think about interfaces, brand, and type — design as a system, not decoration. Distilled from the Geist design system docs, his one first-person essay, and his own portfolio code into an installable agent skill.

## Install

```
npx skills add tylergibbs1/evilrabbitdesin
```

Or clone directly into your skills directory:

```
git clone https://github.com/tylergibbs1/evilrabbitdesin.git \
  ~/.claude/skills/evilrabbitdesin
```

## Skills

### [evil-rabbit-design](skills/evil-rabbit-design/SKILL.md)

**Design and review like Evil Rabbit / Geist.** Ten core principles — constraints as the tool, system over novelty, function over gimmick, monochrome by default, structure from borders not shadows — plus a copy-paste review checklist, the exact Geist tokens, the brand/visual language, and honestly-scoped sources.

| You'll learn | From |
|---|---|
| Constraints are the design tool, not a limitation | Geist Pixel essay (his own words) |
| System over novelty — nothing ships that breaks the rhythm | Geist Pixel essay |
| Function over gimmick; craft is manual attention | Geist Pixel essay |
| Monochrome foundation; color only when it carries meaning | Geist system / `vercel.com/design` |
| Structure from 1px borders and tonal surfaces, not shadows | Geist system spec |
| Exact tokens: color scales, type scale, 4px spacing, radius, focus ring | `vercel.com/design`, `vercel.com/geist/colors` |
| Geometry and the triangle; brand vs. product color | Vercel brand / `vercel.com/geist/brands` |
| Simplicity, minimalism, speed; Swiss grotesque typography | `vercel.com/font`, `vercel/geist-font` |
| Why imitations of the aesthetic come out flat | His portfolio code + system analysis |

## Usage

Describe a design problem in plain language — the skill triggers on its own:

```
You:    We want our dev-tool landing page to feel like Vercel, so the designer
        made it dark with a purple-blue gradient hero and a neon accent on every
        section. On the right track?

Claude: [evil-rabbit-design triggers]
        That's the cargo-cult version of the look, not the method. The Vercel feel
        comes from a system, not a gradient: monochrome by default (#171717 near-
        black, never pure #000), color only where it carries meaning, structure
        from 1px hairline borders instead of glows...
        → drop the per-section neon; let type and whitespace do the work
        → one purposeful accent (Vercel Blue #006bff), everything else grayscale
```

You can also invoke it explicitly: *"Review this dashboard using the Evil Rabbit / Geist design principles."*

## How skills work

The skill follows the [Agent Skills spec](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview):

```
skills/<skill-name>/
├── SKILL.md           # Main instructions (loaded when triggered)
├── references/        # Detailed guides (loaded on demand)
└── evals/
    └── evals.json     # Evaluation tasks
```

Only the skill metadata is loaded into context at startup. The full SKILL.md is read when the skill triggers. Reference files load only when needed — progressive disclosure keeps your context window clean.

## A note on sourcing

Evil Rabbit gives almost no interviews. This skill is honest about what is and isn't attributable to him:

- **His own words** come mainly from one essay he authored — [Introducing Geist Pixel](https://vercel.com/blog/introducing-geist-pixel) (constraints-as-tool, system over novelty, function over gimmick, manual craft).
- **The Geist system** (color, type, spacing, components) reflects his direction but is documented institutional spec at [vercel.com/design](https://vercel.com/design) — not personal quotes.
- **Geist the typeface** was a directed team effort with [basement.studio](https://basement.studio/post/the-birth-of-geist-a-typeface-crafted-for-the-web), not a solo draw.

Full source list and caveats: [`skills/evil-rabbit-design/references/sources.md`](skills/evil-rabbit-design/references/sources.md).

## Sources

- [Introducing Geist Pixel](https://vercel.com/blog/introducing-geist-pixel) — essay authored by Evil Rabbit (best first-person source)
- [Geist design system](https://vercel.com/design) — machine-readable token spec
- [Geist colors](https://vercel.com/geist/colors) · [introduction](https://vercel.com/geist/introduction) · [typography](https://vercel.com/geist/typography) · [brands](https://vercel.com/geist/brands)
- [Geist font](https://vercel.com/font) · [vercel/geist-font](https://github.com/vercel/geist-font)
- [ZEIT is now Vercel](https://vercel.com/blog/zeit-is-now-vercel) — the rebrand
- [The birth of Geist](https://basement.studio/post/the-birth-of-geist-a-typeface-crafted-for-the-web) — basement.studio
- [evilrabb.it](https://evilrabb.it) · [github.com/evilrabbit](https://github.com/evilrabbit) — his portfolio and code
- [Skill authoring best practices](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices) — Anthropic

## Contributing

1. Fork the repo
2. Create a branch (`feature/skill-name`)
3. Follow the skill structure above — SKILL.md under 500 lines, references one level deep
4. Include evals with realistic tasks (not trivial ones)
5. Submit a PR

## License

MIT
