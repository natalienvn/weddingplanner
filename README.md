# Wedding To-Do

A single-page wedding planning tracker — categories of tasks, each expandable
for notes. No build step, no dependencies: it's one static `index.html` file.

## Run it locally

Just open `index.html` in a browser, or serve the folder with anything static:

```
npx serve .
```

## Deploy to Vercel

**Option A — via GitHub (recommended, so future pushes auto-deploy):**

1. Create a new repo on GitHub and push these files to it:
   ```
   git init
   git add .
   git commit -m "Wedding to-do app"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
2. Go to [vercel.com/new](https://vercel.com/new), click **Import Project**,
   and select the repo.
3. Vercel will detect it as a static site automatically — no framework, no
   build command, no output directory needed. Click **Deploy**.
4. Every future push to `main` will auto-deploy.

**Option B — Vercel CLI, no GitHub needed:**

```
npm i -g vercel
vercel --prod
```
Run that from inside this folder and follow the prompts.

## How saving works

The app saves your data in the browser's local storage (`localStorage`), keyed
as `wedding-todo-data`. That means:

- Changes save automatically as you go — no save button needed.
- Data lives **in that specific browser, on that specific device**. It won't
  sync between your phone and laptop, and clearing browser data / site data
  will erase it.
- If you want it synced across devices, that needs a real backend (e.g. a
  small API + database) — let me know if you want that built out.

## Files

- `index.html` — the whole app (HTML, CSS, and JS in one file)
- `README.md` — this file
