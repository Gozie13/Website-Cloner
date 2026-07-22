# Website Cloner

Clone any website into a clean Next.js and Tailwind project using an AI agent. Point it at a URL, run `/clone-website`, and the agent inspects the site, pulls its design tokens and assets, and rebuilds it section by section.

## How it works

The `/clone-website` skill runs a multi-phase pipeline:

1. Reconnaissance: screenshots, design token extraction, and an interaction sweep (scroll, click, hover, responsive)
2. Foundation: fonts, colors, globals, and downloading all assets
3. Component specs: detailed spec files with exact computed CSS values, states, and content
4. Parallel build: builder agents work in git worktrees, one per section
5. Assembly and QA: merges the work, wires up the page, and diffs it against the original

## Quick start

1. Clone this repo into a new project folder:

   ```bash
   git clone https://github.com/Gozie13/Website-Cloner.git .
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Start the dev server:

   ```bash
   npm run dev
   ```

4. Open the folder in your AI coding editor, then run:

   ```
   /clone-website <target-url>
   ```

5. Customize the result for your project.

## Tech stack

- Next.js 16 (App Router, React 19, TypeScript)
- shadcn/ui (Radix primitives, Tailwind CSS v4)
- Tailwind CSS v4
- Lucide React icons

## Commands

```bash
npm run dev       # Start dev server
npm run build     # Production build
npm run lint      # ESLint check
npm run typecheck # TypeScript check
```

## Note

This is a starting point, not a finished product. Do not pass off another company's brand, logos, or copy as your own, and respect each site's terms of service.

## License

MIT
