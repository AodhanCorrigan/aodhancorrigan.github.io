# Aodhan Corrigan — personal website

A research-first Jekyll website for GitHub Pages. Photography and writing share one section: Photography & Stories.

Start with [How to edit your website](HOW-TO-EDIT.md). All routine updates are simple text files; no HTML editing is required.

This is a fresh draft, not a copy of the old HTML5 UP template. The example project and story are clearly marked and should be replaced before publishing.

## Contents

- `_includes/bio.md`: homepage introduction
- `_research/`: research projects, with optional publication links and figures
- `hobbies.md`: your interests outside research
- `cv.md`: your CV text and optional PDF download
- `_posts/`: photography, photo essays, and written posts
- `_templates/`: copyable starting points, excluded from the website automatically
- `assets/images/`: your photographs and figures
- `_layouts/` and `assets/style.css`: the design; routine updates do not require editing these

## Publishing on your existing GitHub Pages address

Preserve the old `html5up-strata` branch. Put this folder's **contents** at the root of a new branch, for example `research-site`. Do not upload the enclosing `personal-site` folder or generated `_site` folder.

Before switching the live site, replace the labelled examples, check your biography, and add your own images. In the repository's **Settings → Pages**, choose **Deploy from a branch**, then select the new branch and `/ (root)`. If Pages is currently configured to use GitHub Actions, this changes the publishing method; do it only when ready to replace the live site. GitHub's built-in Jekyll build then publishes updates from that branch automatically. No `.nojekyll` file should be present.

GitHub also supports a custom Actions deployment; this small site deliberately needs no custom workflow or plugins.

## Local preview (optional)

With Ruby and Bundler installed:

```sh
bundle install
bundle exec jekyll serve
```

Open the address printed in the terminal. Edit content, refresh the page. Restart after changing `_config.yml`.

Official references: [Jekyll posts](https://jekyllrb.com/docs/posts/) · [Editing on GitHub](https://docs.github.com/en/repositories/working-with-files/managing-files/editing-files) · [Pages publishing source](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
