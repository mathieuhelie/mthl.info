Refresh the mthl.info personal site by synthesizing all available sources and regenerating the CV pages.

## Steps

1. **Read source documents** — Read every file in the `content/` directory. These are the user's primary source of truth: CV documents, work experience notes, project descriptions, client profiles, and anything else dropped there.

2. **Search for new public information** — Run web searches to find updates since the last refresh:
   - Fetch: `thenatureofcities.com/author/mathieuhelie` — the most reliable source for new articles
   - Search: `"Mathieu Hélie" site:thenatureofcities.com` — cross-check
   - Compare results against the known article list below and note any additions

3. **Synthesize** — Combine content/ documents + search findings + the known baseline below into a coherent, up-to-date professional narrative. The master history lives in `src/index.md`. Variant pages are filtered views of the same history — same voice, same language, same first-person perspective. They do not adopt a different tone or target a different "audience voice."

4. **Regenerate the three public CV pages**:
   - `src/index.md` — Full chronological CV, maximum detail. Every role, every article, all education, all writing. SEO-optimized home page.
   - `src/cv-tech.md` — Filter to tech/consulting content. Lead with platform architecture and dev roles. Urbanism compressed to one brief mention. Same voice as index.md.
   - `src/cv-urban.md` — Filter to urbanism/complexity science content. Lead with TNOC articles and Emergent Urbanism. Tech career compressed to one brief paragraph. Same voice as index.md.

5. **Update `src/cv-linkedin.md` separately** — This is a working reference document for updating LinkedIn manually. It is NOT published in the site navigation. Keep it structured as: About, Experience, Education, Skills, Publications. It should reflect the same facts as index.md but formatted for copy-paste into LinkedIn.

6. **Keep the front matter** — Every page must keep its YAML front matter (layout, title, description, variant). Update `title` and `description` if the content warrants it.

7. **Build** — Run `npm run build` and confirm it completes without errors.

8. **Do not push or commit** — The user manages commits and pushes themselves.

---

## Content rules

- **No hallucination** — Do not invent details not present in source documents. If a thesis title, date, or project detail isn't in content/ or the known baseline, omit it rather than invent it.
- **No fabricated Medium articles** — Only include Medium articles explicitly confirmed (see baseline below). Do not add articles not listed.
- **No roundtable contributions** — Do not list minor TNOC contributions (book recommendations, roundtables) as publications.
- **Thesis description** — Describe the thesis content without inventing or asserting a specific title. Use: "Examined how emergent phenomena, complex adaptive systems, and fractal geometry explain the structure and growth of traditional and organic urban forms, in contrast to top-down planned cities."
- **"Working remotely"** — Do not add this to the intro. Location is Montreal, Canada — nothing more.
- **Consistent voice** — All pages use the same first-person professional voice. Variant pages filter content, not tone.

---

## Known Baseline

### Career (reverse chronological)

- **Appnovation Technologies** — Senior Associate Technology, April 2020–present. Sub-roles (not all for Pfizer):
  - Tech Lead — Pfizer Internal Platform, 2025–present (team of 5–8, LiteLLM, Vue.js, Laravel)
  - Pfizer Platform Integration Consultant, 2023–2024 (cancer PWA, PfizerForAll.com, Japan COVID portal, Angular/Ionic/Drupal/Laravel/Vue.js)
  - Cloud & Web Application Architect — Pfizer, 2023 (serverless AWS portal, Remix/React/TypeScript/PostgreSQL/AWS Lambda)
  - Platform Architect, Decoupled Web, 2022 (federated search, headless CMS, Drupal/Node.js/Docker/GCP/Contentful/Next.js/Svelte)
  - Tech Lead — Platform Operations, 2021 (containerized AWS hosting, Drupal/Docker/AWS OpenShift)
  - JavaScript Integration Lead, 2020 (drag-and-drop CMS, GatsbyJS/GraphQL/React/Firebase/GCP)
- **Self Employed** — Consultant Developer, June 2019–March 2020 (Mediawiki, PHP, Svelte, Platform.sh)
- **SERTI (Cogeco Inc.)** — Senior Drupal Developer Consultant, February 2018–May 2019 (Drupal 8/Symfony/PHP/React/Redux/PHPUnit)
- **Appnovation Technologies** — Senior Developer, December 2016–February 2018 (Canadian Red Cross, Carrefour, SWIFT, Agropur; Drupal 8/Symfony/PHP)
- **Floe Design + Technologies** — Drupal Technical Lead, March 2015–November 2016 (Digital.NYC/StartHubBoston; Drupal 7&8/PHP/ElasticSearch)
- **Agence Webdiffusion** — Co-Founder & Web Architect, June 2013–May 2018 (side venture; Drupal 7/Aegir)
- **dbn.ca** — Lead Web Developer, 2010–2013 (Drupal 6&7/PHP/MySQL)

### Education

- Institut d'Urbanisme de Paris / Université Paris I Panthéon-Sorbonne — Master's, Urban Planning, 2008
- Concordia University — B.A., Economics and Computer Science, 2006 (Montreal)
- Champlain Regional College — DEC, Computer Science, 2002 (Saint-Lambert)
- SAJE — Certificate in Sales Consulting / Entrepreneurship, 2013–2014

### Known articles at The Nature of Cities

1. Explaining the Housing Crisis with the Theory of Constraints — Apr 2023 — https://www.thenatureofcities.com/TNOC/2023/04/11/explaining-the-housing-crisis-with-the-theory-of-constraints/
2. A Fractal Solution to Regional Complexity and Governance — Jan 2020 — https://www.thenatureofcities.com/TNOC/2020/01/23/a-fractal-solution-to-regional-complexity-and-governance/
3. Neighborhoods that Change in Non-linear Ways — Jul 2019 — https://www.thenatureofcities.com/TNOC/2019/07/10/neighborhoods-that-change-in-non-linear-ways-urban-planning-for-succession/
4. Neural Networks — A New Model for 'The Kind of Problem a City Is' — Apr 2018 — https://www.thenatureofcities.com/2018/04/29/neural-networks-new-model-kind-problem-city/
5. The Effect of Iteration on Urban Form, Part II — Jun 2017 — https://www.thenatureofcities.com/2017/06/28/effect-iteration-urban-form-part-ii-iteration-ecosystem/
6. The Effect of Iteration on Urban Form, Part I — Jun 2017 — https://www.thenatureofcities.com/2017/06/25/effect-iteration-urban-form-part/
7. Uses and Abuses of Preservation — Nov 2016 — https://www.thenatureofcities.com/2016/11/13/uses-and-abuses-of-preservation/
8. Common Threads: Jane Jacobs and Elinor Ostrom — May 2016 — https://www.thenatureofcities.com/TNOC/2016/05/28/common-threads-connections-among-the-ideas-of-jane-jacobs-and-elinor-ostrom-and-their-relevance-to-urban-socio-ecology/

### Other writing

- Emergent Urbanism blog — http://emergenturbanism.com (since 2007)
- Medium: "Lean Drupal Development" — https://medium.com/@mathieuhelie/lean-drupal-development-finish-your-drupal-projects-in-half-the-time-a98eaaede088
- SlideShare: https://www.slideshare.net/mhelie

### Links

- GitHub: https://github.com/mathieuhelie
- LinkedIn: https://www.linkedin.com/in/mhelie
- Twitter/X: https://twitter.com/mathieuhelie
- Email: mthl@mthl.info

---

## Style guidelines

- **Headers**: `##` for sections, `###` for roles/articles, `####` for org/date metadata lines
- **Dates**: `#### Montreal, Canada | 2013–2018`
- **Links**: All TNOC article titles must be hyperlinks to their canonical URLs
- **No placeholders**: Omit dates rather than guess. content/ docs are authoritative.
- **index.md**: Comprehensive. 800–1500 words of body content.
- **cv-tech.md**: Concise but complete on tech. 400–700 words.
- **cv-urban.md**: Article-heavy, thesis-forward. 400–600 words.
- **cv-linkedin.md**: Structured for copy-paste. `---` dividers between experiences.
