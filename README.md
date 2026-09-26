# CRAFT Prompt Builder: Ministry AI Blueprint

A single-page static web app that generates a CRAFT prompt (Context, Role, Action, Format, Target audience) for a one-page ministry AI strategy blueprint. The interface and the generated prompt are available in English and Bahasa Melayu (DBP standard).

No build step, no backend and no API keys. It runs entirely in the browser, so it fits comfortably within the Vercel free (Hobby) tier.

## Files
- `index.html` — the whole app (HTML, CSS and JavaScript)

## Deploy on Vercel

### Option A: GitHub + Vercel dashboard
1. Create a new GitHub repository and upload `index.html` (and this README).
2. Go to https://vercel.com/new and import the repository.
3. Framework preset: **Other**. Leave the build command and output directory empty.
4. Click **Deploy**. Every push to the main branch redeploys automatically.

### Option B: Vercel CLI
```bash
npm i -g vercel
cd craft-prompt-builder
vercel          # preview deployment
vercel --prod   # production deployment
```

## Run locally
Open `index.html` directly in a browser, or serve the folder:
```bash
python -m http.server 8000
```

## Notes
- Drafts are saved in the browser's localStorage, so each user's inputs stay on their own device.
- Empty fields remain as [placeholders] in the prompt, highlighted in the preview.
- The example content describes an illustrative scenario only. Acronyms (Akta 864, AIaaS JDN, GPAISA, RPSA 2026–2030) are kept as on the source slide.
- To change wording, edit the `T` (interface text), `PH` (placeholders), `DEFAULTS`, `buildEN()` and `buildMS()` objects in the script.
