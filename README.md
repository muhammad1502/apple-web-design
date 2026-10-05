# apple-web-design

An apple.com-style design system, starter site and test suite, packaged as a
[Claude skill](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills).
Give it to Claude and ask for a site; it builds one that looks and behaves
like this, and checks its own work.

## What you get

- **Design system:** colour tokens with matched light and dark themes, Apple's
  type scale and breakpoints, one button system, cards, a translucent sticky
  nav and a footer.
- **Features:** phone section chips, a ⌘K / Ctrl+K command palette, details
  modals that become swipeable bottom sheets on phones, card carousels,
  count-up stats, a back-to-top progress ring and a sun-to-moon theme switch
  with a crossfade.
- **Motion that never hides content:** scroll-linked and interaction-driven
  only, and off under reduced motion.
- **UX psychology:** layout and interactions follow growth.design's principles
  (Hick's Law, Progressive Disclosure, Chunking, Fitts's Law and more), mapped in
  `references/ux-principles.md`.
- **Quality built in:** WCAG 2.2 AA, pre-rendered HTML, self-hosted fonts, a
  strict Content Security Policy, real 404s and Vercel-ready config.
- **Starter template** (`assets/template/`): Vite 8 + React 19 + TypeScript 7.
  One data file (`src/site-data.ts`) drives the hero and any number of
  sections: text, feature tiles, cards, lists and contact.
- **Test suite** (`scripts/qa.mjs`): a content-agnostic Playwright and axe
  suite (481 checks on the template) covering 15 screen widths, both themes,
  keyboard paths, accessibility, motion and security.
- **Brand assets** (`scripts/brand-assets.mjs`): favicon, touch icon and a
  1200×630 share image from a name and tagline.

## Install

**Claude Code, for all your projects**

```bash
git clone https://github.com/muhammad1502/apple-web-design ~/.claude/skills/apple-web-design
```

**Claude Code, for one project:** clone it into that project's
`.claude/skills/apple-web-design` instead.

**Claude apps (web, desktop, mobile):** download this repository as a zip,
rename the top folder inside it to `apple-web-design`, zip it again, then go
to **Customize → Skills → + → Create skill → Upload a skill**. Code execution
must be on (**Settings → Capabilities**).

## Use

Ask for what you want. For example:

- "Build a landing page for my bakery in the apple-web-design style."
- "Restyle my existing site with this design system, keeping my content."

Claude starts from the template, swaps in your real content, generates the
icons and share image, runs the test suite and fixes anything it reports.
Start with "Use the apple-web-design skill…" to be sure it's picked up.

## Run the template yourself

```bash
cp -r assets/template my-site && cd my-site
npm install
npm run dev     # http://localhost:5173
npm run build   # type-check, build, pre-render into dist/
```

Node 20.19+ or 22.12+. It deploys to Vercel as is.
