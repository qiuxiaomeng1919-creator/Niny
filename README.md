# Niny (Xiaomeng) Qiu — CV site

A single-page CV and portfolio. Everything is contained in `index.html`: the
photographs, company marks, university crests and project figures are all
embedded in the file itself, so there is nothing else to upload and no build
step.

The only thing loaded from the internet at runtime is the typefaces
(Newsreader and IBM Plex, from Google Fonts). If that request fails the page
still works, it just falls back to system fonts.

## Putting it on GitHub Pages

**Option A — through the website, no software needed**

1. Sign in to GitHub and create a new repository.
   Name it `qiuxiaomeng1919-creator.github.io` if you want the short address
   `https://qiuxiaomeng1919-creator.github.io`. Any other name works too, and
   gives you `https://qiuxiaomeng1919-creator.github.io/<repo-name>/`.
2. Set it to **Public**. GitHub Pages needs a paid plan to publish from a
   private repository.
3. On the repository page choose **Add file → Upload files**, drag in
   `index.html` and this `README.md`, then **Commit changes**.
4. Go to **Settings → Pages**. Under *Build and deployment*, set
   *Source* to **Deploy from a branch**, branch **main**, folder **/ (root)**.
   Save.
5. Wait a minute or two, then reload that page. The address appears at the top.

**Option B — from the command line**

```bash
cd path/to/this/folder
git init
git add .
git commit -m "Add CV site"
git branch -M main
git remote add origin https://github.com/qiuxiaomeng1919-creator/<repo-name>.git
git push -u origin main
```

Then follow step 4 above to switch Pages on.

## Updating it later

Replace `index.html` with a newer copy and commit again. GitHub Pages
republishes within a minute or so. A hard refresh (Ctrl+F5) clears the old
cached version if you still see it.

## A note on what becomes public

A public repository makes everything in it readable by anyone, including the
email address and links on the page and every photograph embedded in it. That
is the intent here, but it is worth knowing that the boxing and live music
photographs contain other identifiable people.

Do not commit the original photo folders from the working directory. They are
around 115 MB of full resolution files and are not needed: the versions used
by the page are already inside `index.html`. The included `.gitignore` keeps
them out if you ever copy them in.
