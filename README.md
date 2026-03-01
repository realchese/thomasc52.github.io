# Thomas Chan — Personal Blog

A clean editorial blog built with [Hugo](https://gohugo.io/) and the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme, deployed on GitHub Pages.

## Run Locally

```bash
# Install Hugo (macOS)
brew install hugo

# Start dev server
hugo server -D
```

Then open http://localhost:1313/

## Deploy to GitHub Pages

1. Create a new GitHub repo (e.g. `thomas-blog` or `yourusername.github.io`)
2. Push this project:
   ```bash
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/YOURUSERNAME/thomas-blog.git
   git branch -M main
   git push -u origin main
   ```
3. In your repo's **Settings → Pages**, set Source to **GitHub Actions**
4. The included `.github/workflows/deploy.yml` handles the rest automatically
5. Your site will be live at `https://YOURUSERNAME.github.io/thomas-blog/`

**Want it at `yourusername.github.io` (no `/thomas-blog/`)?** Name the repo `yourusername.github.io` instead, and update `baseURL` in `hugo.toml` to `https://yourusername.github.io/`.

## Add a New Article

1. Create a new file in `content/posts/`, e.g. `content/posts/my-new-essay.md`
2. Add frontmatter at the top:
   ```markdown
   ---
   title: "My New Essay"
   date: 2025-03-15
   draft: false
   description: "A short summary of the essay."
   ---

   Your essay text goes here.
   ```
3. Commit and push. GitHub Actions will deploy automatically.

## Project Structure

```
thomas-blog/
├── hugo.toml              # Site config
├── content/
│   ├── about.md           # About page
│   └── posts/             # Essays go here
│       ├── it-should-be-those-damn-phones.md
│       ├── alysa-liu-value-driven-mentality.md
│       └── humans-are-only-so-much-theory.md
├── themes/PaperMod/       # Theme (git submodule)
└── .github/workflows/     # Auto-deploy config
```
