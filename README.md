# half.

Static storefront prototype pages for `half.`:

- `index.html` (homepage)
- `signin.html` (Google sign-in)
- `airpods.html`
- `jbl.html`
- `applewatch.html`
- `nike.html`

## Why you still may not see files on GitHub

In this environment, commits were created only in the local Git repo on branch `work`.
There is currently **no remote configured**, so nothing has been uploaded yet.

Also, if you push only `work`, GitHub will still open on `main` by default unless you switch branches in the UI.

## Confirm local commits exist

```bash
git log --oneline --decorate -n 5
```

You should see commits including:

- `Add half storefront pages with Firebase auth and reviews`
- `Add README with GitHub publishing steps for branch visibility`

## Publish to your GitHub repo

Run these commands on your machine (where you are logged in to GitHub):

```bash
git remote add origin <your-github-repo-url>
git push -u origin work
```

Then open your GitHub repo and switch the branch dropdown from `main` to `work`.

## If you want files on `main`

```bash
git checkout -b main work
git push -u origin main
```

Or create a Pull Request from `work` -> `main` in GitHub.

## Local preview

```bash
python -m http.server 4173
```

Open `http://localhost:4173/index.html`.
