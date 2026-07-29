# Ernesto Criado-Hidalgo

Source for [ernestocriado.github.io](https://ernestocriado.github.io/), a personal research website focused on engineering non-invasive tools for biology and medicine.

The site includes:

- research directions and selected projects
- experience, education, and technical methods
- featured papers and a complete publication list
- writing on ultrasound, mechanobiology, data science, and AI-assisted research
- downloadable CV and resume

## Local Preview

The site uses Hugo, Hugo Blox, and Tailwind CSS. After installing Node.js, Go, and Hugo Extended:

```bash
corepack pnpm install
corepack pnpm run dev
```

Open [http://localhost:1313](http://localhost:1313). See [LOCAL_PREVIEW_WORKFLOW.md](LOCAL_PREVIEW_WORKFLOW.md) for the complete branch and troubleshooting workflow.

## Production Build

```bash
corepack pnpm run build
```

Pushing `main` deploys the site through the GitHub Pages workflow in `.github/workflows/deploy.yml`.

## Content

Page content is stored in `content/`, site configuration in `config/_default/`, and visual overrides in `assets/css/custom.css` and `layouts/`.

Personal writing, research figures, photographs, videos, CV, and resume are copyright Ernesto Criado-Hidalgo unless otherwise credited. The underlying site code retains the MIT license and attribution provided in [LICENSE.md](LICENSE.md).
