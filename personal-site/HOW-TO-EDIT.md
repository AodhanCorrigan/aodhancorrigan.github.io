# How to edit your website

Once this website is in GitHub, you can do all of this in your browser. Select the website's publishing branch first. Open a file and click the pencil to edit it; **Commit changes** saves it. Changes on the publishing branch trigger an automatic site rebuild, which usually takes a short while.

GitHub's Markdown preview shows your text, not the complete website design. The live website uses the site's layouts. If you want to review a change without publishing it, save it on a different branch first.

## 1. Write your introduction

Edit `_includes/bio.md`. Replace the italic placeholder with two or three sentences about yourself and your research. This text appears beneath your name on the homepage.

The affiliation is already set to University of Waterloo / Institute for Quantum Computing. If it changes, update `index.html` and `research/index.html`.

## 2. Add a research project

1. Open `_templates/research-project.md` and copy its contents.
2. Choose **Add file → Create new file** and name it `_research/my-project.md`.
3. Paste the template. Change the title, summary, and other fields between the `---` lines.
4. Write the longer explanation below the second `---`.
5. Save with **Commit changes**.

The site automatically adds the project to the Research Projects page. Smaller `order` numbers appear first. Use different numbers to choose the order.

Keep quotation marks around text fields. To put a double quote inside a title, write `\"`.

### Publications and figures are optional

- `publication`: a citation in whatever style you prefer.
- `paper_url`: the full link to your paper, preprint, or PDF.
- `image`: a path such as `/assets/images/my-plot.png`.
- `image_alt`: describe what the plot or photograph communicates.
- `caption`: an optional caption beneath the image.

Leave any unused field as `""`. A publication link appears when both `publication` and `paper_url` are filled in. A figure is displayed only when `image` is filled in. For extra papers or figures, use Markdown links and images in the body.

Upload figures first: open `assets/images`, choose **Add file → Upload files**, and save. PNG is useful for plots; JPG or WebP for photographs. Use lowercase filenames with hyphens instead of spaces.

Delete `_research/example-project.md` when your real project is ready, or edit that example and remove `example: true`.

## 3. Add photography or a story

1. Upload your photographs to `assets/images`.
2. Copy `_templates/photo-story.md`.
3. Create `_posts/2026-09-18-my-story.md`, using your actual publication date and a short filename.
4. Set the title, summary, cover image, image description, and optional caption.
5. Write below the second `---`, or leave the body empty for a single photograph.

The latest entries appear first. The title does not need to match the filename exactly. Dates in the future are not published until a build occurs after that date; use today's date for immediate publishing.

For a writing-only post, set `cover`, `cover_alt`, and `cover_caption` to `""`. Its listing will use a simple text tile. For a photo essay, add images between paragraphs:

```markdown
![A description of what the photograph shows](/assets/images/my-photo.jpg)

*An optional caption.*
```

Delete `_posts/2026-09-18-example-story.md` when you have your own entry, or replace its contents and remove `example: true`.

## 4. Markdown basics

```markdown
## A section heading

An ordinary paragraph. **Bold** and *italic* text.

[Link text](https://example.com)

- One item
- Another item
```

Keep the opening and closing `---` lines in each template. They separate the page settings from your writing. You do not need to edit the layouts or CSS to add content.

## Before making the draft public

Replace the homepage blurb and both examples. The boxes labelled “Your photographs here” and “Research figure or photograph” are explicit layout placeholders, not images; they disappear when you supply images or remove the examples.

Everything committed to this public repository, including drafts and image metadata, is publicly readable. Upload web-sized copies of photos (roughly 1600–2400 pixels on the long side) and remove location metadata if you do not want to share it.

## Hobbies and CV

Edit `hobbies.md` for your hobbies page. Replace the placeholder with your interests and add headings, paragraphs, links, and images using the same Markdown syntax as stories. The commented example in that file provides a starting point.

Edit `cv.md` for your CV page. Suggested headings are included in a comment; copy them outside the `<!-- ... -->` comment markers to make them visible. You can write the CV directly on the page, offer a PDF download, or do both.

For a PDF, upload your CV to `assets/cv.pdf`, then change the `pdf: ""` line at the top of `cv.md` to `pdf: "/assets/cv.pdf"`. The download link stays hidden until you provide a path. Keep the filename the same when replacing your CV later.
