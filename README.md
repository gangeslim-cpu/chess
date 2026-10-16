# Wizard Chess 3D — Sanctum Edition

Interactive 3D Gothic Cathedral Wizard Chess featuring sculpted stone pieces, cinematic magical battle captures, stone shatter physics, dynamic Chiaroscuro cathedral lighting, and single-player AI.

## Why might it fail on GitHub / GitHub Pages? (Troubleshooting)

1. **Vite Base Path for Subdirectories**:
   When hosting on GitHub Pages at `https://<username>.github.io/<repository-name>/`, root-relative asset URLs (`/assets/...`) result in `404 Not Found` errors.
   - **Fix**: `vite.config.ts` includes `base: './'` and asset loading uses `import.meta.env.BASE_URL` so all assets are resolved relatively.

2. **Node & Dependencies**:
   - Ensure Node.js (v18+) is installed.
   - Run `npm install` followed by `npm run build` or `npm run dev`.

3. **Automatic Deployment to GitHub Pages**:
   - A pre-configured GitHub Actions workflow is included at `.github/workflows/deploy.yml`. When you push to `main` or `master`, it automatically builds and deploys your game to GitHub Pages.
   - In your GitHub repository settings under **Pages**, set the source to **GitHub Actions**.

## Local Development

```bash
npm install
npm run dev
```
Open `http://localhost:3000` in your browser.
