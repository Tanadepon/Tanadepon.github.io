# Repository Guidelines

## Project Structure & Module Organization

This is a static personal portfolio using Astro 7, Tailwind CSS 4, and strict TypeScript. The current homepage is intentionally blank so the owner can design it.

- `src/pages/index.astro`: homepage; additional `.astro` files in `src/pages/` become routes.
- `src/styles/global.css`: global stylesheet, currently containing the Tailwind import.
- `public/`: static assets served directly, such as `/profile.jpg`. The existing root-level `Profile.jpg` must be moved or imported appropriately before use on a page.
- `astro.config.mjs`: Astro configuration and Tailwind Vite plugin.
- `tsconfig.json`: extends Astro's strict TypeScript configuration.
- `dist/`, `.astro/`, and `node_modules/`: generated output; do not edit or commit.

Add reusable components to `src/components/` when needed; avoid creating unused scaffolding.

## Build, Test, and Development Commands

Use `npm.cmd` instead of `npm` in Windows PowerShell if script execution is restricted.

- `npm ci`: install the exact dependencies in `package-lock.json`.
- `npm run dev`: start local development with automatic updates on save.
- `npm run check`: run Astro diagnostics and TypeScript checks.
- `npm run build`: generate the production site in `dist/`.
- `npm run preview`: serve the latest production build; rebuild to see changes.
- `npm audit`: inspect dependency security advisories.

## Coding Style & Naming Conventions

Use two-space indentation. Keep Astro imports and TypeScript logic in the frontmatter block. Follow existing single-quoted JavaScript imports and double-quoted HTML attributes. Use semantic HTML, descriptive alternative text, and keyboard-accessible controls.

Use PascalCase component filenames, such as `ProjectCard.astro`, and lowercase route filenames. Prefer Tailwind utilities for layout and shared CSS for site-wide rules. No formatter or linter is configured.

## Testing Guidelines

No automated test framework or coverage threshold is configured. Run `npm run check` and `npm run build` before submitting changes. For visual changes, inspect desktop and mobile layouts, keyboard navigation, and links using the development server. Add focused tests if introducing nontrivial behavior; no test naming convention exists yet.

## Commit & Pull Request Guidelines

This checkout has no Git history, so no established commit convention can be inferred. Use concise imperative messages, such as `Add research section`. Pull requests should describe the change, include validation results, link relevant issues, and attach screenshots for visual changes.

## Scope & Configuration

Preserve the blank starting point until a design is requested. Do not invent personal claims or sample projects. Keep secrets out of source control, and commit lockfile updates alongside dependency changes.
