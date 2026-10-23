# Personal portfolio

A blank Astro project with Tailwind CSS and strict TypeScript.

## Develop

```sh
npm install
npm run dev
```

On Windows PowerShell with restricted scripts, use `npm.cmd` instead of `npm`.

Add your design to `src/pages/index.astro` and styles to `src/styles/global.css`.

## Validate and build

```sh
npm run check
npm run build
npm run preview
```

The production output is generated in `dist/`.

## Publish to GitHub Pages

This project is configured for https://tanadepon.github.io using a repository
named `Tanadepon.github.io` owned by `Tanadepon`.

1. Create an empty public repository named `Tanadepon.github.io` on GitHub.
2. From this project folder, run:

   ```sh
   git init -b main
   git add .
   git commit -m "Prepare portfolio for GitHub Pages"
   git remote add origin https://github.com/Tanadepon/Tanadepon.github.io.git
   git push -u origin main
   ```

3. In the repository, open **Settings > Pages** and set **Source** to
   **GitHub Actions**.
4. Open **Actions > Deploy to GitHub Pages**. If the initial run failed before
   Pages was enabled, rerun it. Once deployment succeeds, visit
   https://tanadepon.github.io.

Future pushes to `main` automatically validate, build, and deploy the site using
`.github/workflows/deploy.yml`. Keep the repository name above so the site is
served at the domain root without an additional path.
