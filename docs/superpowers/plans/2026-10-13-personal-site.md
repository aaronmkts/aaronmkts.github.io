# Personal research website implementation plan

**Goal:** Personalise the existing al-folio website for Aaron M. Thomas.

**Approved direction:** Retain the academic template and portrait. Present quantum machine learning, generative AI and agentic AI interests; Birmingham and QunaSys affiliations; supervisors Dr. Sharu Jose and Dr. Ronin Wu. Publish experience as prose, with no CV download or telephone number. Keep personal interests on their own page.

**Architecture:** Existing Jekyll layouts, Markdown pages, project/news collections and BibTeX publications. No replacement framework or hosting provider.

## Implementation

- [x] Configure identity, contact, metadata and the root GitHub Pages URL in `_config.yml`; exclude unused template content from the build.
- [x] Populate `_pages/about.md`; add Experience and Personal pages; customise Projects and Publications navigation.
- [x] Add three project pages for VAE-QWGAN, Same Graph Different Likelihoods, and QCA-MolGAN, grounded in publisher/arXiv records.
- [x] Add a personal bibliography and dated news with source links. Use paper publication dates, not inferred acceptance dates.
- [x] Copy the supplied portrait unchanged into `assets/img/aaron-thomas.jpeg`; give it meaningful alternative text.
- [x] Document future news/project updates in README, including the no-CV policy.
- [x] Build with Ruby 3.2 in Docker, inspect desktop/mobile views, check links and absence of example/CV content, then review the diff.

## Sources and editorial decisions

- Name, supervisors, current affiliations and agentic AI interest: user confirmation, 13 October 2026.
- Career dates and education: supplied CV, used privately as source material.
- VAE-QWGAN: https://doi.org/10.1007/s42484-025-00314-z (published 18 September 2025).
- NII: https://arxiv.org/abs/2604.05613 (submitted 7 April 2026; AISTATS calibration workshop, not main conference).
- QCA-MolGAN: https://arxiv.org/abs/2509.05051 and https://ieeexplore.ieee.org/abstract/document/11344621.
- Sparse fine-tuning: https://aclanthology.org/2025.acl-long.1541/.
- Quantum classifier generalisation: https://arxiv.org/abs/2504.17690.
- Omit the CV's ORCID link pending clarification: its identifier appears assigned to a coauthor in publication metadata.

## Validation

Run a production Jekyll build. Inspect each generated page and local navigation; confirm the three intended project routes, correct social links, portrait and metadata. Confirm `/cv/`, demo pages, sample projects and sample PDFs are absent from output. Inspect desktop and mobile screenshots, mobile navigation and light/dark mode. Run `git diff --check` and review only the scoped changes.

## Review and results

- Production build passes using the repository's locked dependencies and Ruby 3.2. The current upstream Docker image uses Ruby 4 and different dependency versions, so it was not used for final verification.
- Sass already compresses `main.css`. Excluding that file from a redundant jekyll-minifier pass reduced the measured build from 214 seconds to 8 seconds (the latter also reused generated image sizes).
- Browser checks pass for nine routes at 1440px and 390px widths: links, portrait, three project cards, five publication entries, mobile navigation, search, dark-mode toggle and absolute Open Graph image URL.
- No JavaScript page errors or horizontal overflow were detected on those routes. Desktop, mobile, project and dark screenshots were visually inspected.
- CV, sample PDF/JSON, blog, sample project and HTML/Plotly demo routes are absent from the generated site. The supplied CV was not copied into the repository. Portrait checksums match the supplied image.
- `git diff --check` passes. Changes reuse existing template components and introduce no application dependencies.
