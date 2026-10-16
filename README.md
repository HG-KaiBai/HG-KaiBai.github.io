# Yixing Zhao's academic website

Source for [hg-kaibai.github.io](https://hg-kaibai.github.io/), built with Hugo and a locally bundled PaperMod theme. GitHub Actions builds and deploys the site to GitHub Pages.

## Repository layout

```text
.github/workflows/hugo.yml   GitHub Pages build and deployment
archetypes/                 Starting points for new research entries
assets/css/                 Site-specific styles
content/
  publications/             Research papers and preprints
  presentations/            Conference talks and abstracts
  teaching.md               Teaching experience
  experience.md             Education, service, and awards
layouts/                    Site-specific template overrides
static/
  cv.pdf                    Current academic CV download
  images/profile.jpg        Homepage portrait
  favicon*                  Browser icons
themes/PaperMod/            Bundled theme and its license
config.yml                  Site metadata, navigation, and homepage
```

## Preview and build

Use Hugo **0.147.2 extended**, matching the deployment workflow. Run from this directory:

```sh
hugo server
```

Open the local address printed by Hugo. To check the production build:

```sh
hugo --minify
```

Hugo generates `public/` and `resources/`; these are ignored and should not be committed. Node.js and Dart Sass are not needed for this site's CSS assets.

## Update content

- Edit the biography, contact links, and navigation in `config.yml`.
- Edit teaching and experience in their Markdown files under `content/`.
- Create a talk with `hugo new content presentations/talk-name/index.md --kind presentation`.
- Create a paper with `hugo new content publications/paper-name/index.md --kind paper`.
- Keep each paper or talk's PDFs, figures, and slides beside its `index.md`, and link to their filenames from that page.
- Set `draft: false` when a new entry is ready to publish. Add `math: true` to an individual page only if it needs equation rendering.

The previous `/papers/`, `/courses/`, and `/presentation/ssc-2026/` addresses redirect to the reorganized pages.

The navigation and homepage **CV** buttons link to `static/cv.pdf`, served at [hg-kaibai.github.io/cv.pdf](https://hg-kaibai.github.io/cv.pdf). This is a copy of `../academic-cv/Yixing_Zhao_Academic_CV.pdf`. After editing the academic CV, refresh this copy before deploying. From the workspace root, `./build.ps1` rebuilds both job resumes and the academic CV and refreshes the website copy; `./academic-cv/build.ps1` rebuilds only the academic CV and refreshes the copy.

## GitHub Pages

In the repository's **Settings → Pages**, select **GitHub Actions** as the build source. Push changes to `main` to run `.github/workflows/hugo.yml`, or start it manually from the Actions tab. Only the generated `public/` directory is deployed.

## Attribution

The site uses Pascal Michaillat's minimalist academic website template and the PaperMod theme. Retain [the template license](LICENSE.md) and [the PaperMod license](themes/PaperMod/LICENSE).
