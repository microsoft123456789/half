# half.

Static storefront prototype pages for `half.`:

- `index.html` (homepage)
- `signin.html` (Google sign-in)
- `airpods.html`
- `jbl.html`
- `applewatch.html`
- `nike.html`

## Why pull requests can look wrong in this environment

This workspace can create local commits, but it does **not** have a GitHub remote configured by default.
So any PR text generated in this environment is only a local artifact unless you push your branch to GitHub.

Also, if the branch is renamed to `work`, GitHub will still show `main` by default until you either:

- switch the branch selector to `work`, or
- open a PR from `work` into `main`.

## Verify current local state

```bash
git branch --show-current
git log --oneline --decorate -n 5
git remote -v
```

If `git remote -v` is empty, nothing has been published yet.

## Publish branch and create a real GitHub PR

```bash
git remote add origin <your-github-repo-url>
git push -u origin work
```

Then on GitHub:

1. Open your repository.
2. Choose branch `work` to confirm files are visible.
3. Click **Compare & pull request** (base: `main`, compare: `work`).

## Optional: put files directly on `main`

```bash
git checkout -b main work
git push -u origin main
```

## Local preview

```bash
python -m http.server 4173
```

Open `http://localhost:4173/index.html`.
