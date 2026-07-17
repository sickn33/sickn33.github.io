# sickn33.github.io

This user-site repository hosts the compatibility bridge from the former
`/antigravity-awesome-skills/` identity to the canonical
`/agentic-awesome-skills/` site.

The generated deployment surface is limited to:

- `.nojekyll`
- `redirect-manifest.json`
- `antigravity-awesome-skills/**`

Scheduled automation regenerates those paths from
[`sickn33/agentic-awesome-skills`](https://github.com/sickn33/agentic-awesome-skills),
opens a fixed-branch pull request when drift exists, dispatches an exact-head
verification, merges only after the protected check succeeds, and verifies the
resulting GitHub Pages deployment. `README.md` and `.github/**` are never part
of the generated sync set.

This user-site repository preserves search and bookmark continuity for the
Agentic Awesome Skills rename.

Requests under `/antigravity-awesome-skills/` receive a static HTML redirect
and canonical link to the matching route under `/agentic-awesome-skills/`.
The redirect set is generated from the canonical skill catalog plus its curated sitemap by
`agentic-awesome-skills`'s `pages:redirect-bridge` maintainer command; see
`redirect-manifest.json` for the exact source and route mapping.
