Refresh the mthl.info personal site by synthesizing all available sources and regenerating the CV pages.

## Steps

1. **Read source documents** — Read every file in the `content/` directory. These are the user's primary source of truth: CV documents, work experience notes, project descriptions, client profiles, and anything else dropped there.

2. **Search for new public information** — Run web searches to find updates since the last refresh:
   - Search: `"Mathieu Hélie" site:thenatureofcities.com` — find any new articles
   - Search: `"Mathieu Hélie" thenatureofcities.com` — catch any not indexed under the exact slug
   - Search: `Mathieu Hélie Appnovation OR Serti` — look for any new public announcements
   - Compare results against the known article list below and note any additions

3. **Synthesize** — Combine content/ documents + search findings + the known baseline below into a coherent, up-to-date professional narrative.

4. **Regenerate the four CV pages**:
   - `src/index.md` — Full chronological CV, maximum detail. Include every role, every article, education, all writing. This is the SEO-optimized home page.
   - `src/cv-tech.md` — Tech/consulting focus. Leads with Drupal/PHP/JS experience, platform architecture, specific projects. Urbanism appears only as "other interests."
   - `src/cv-urban.md` — Urbanism/complexity science focus. Leads with TNOC articles, Emergent Urbanism, thesis, BIMBY.fr. Tech career compressed to one paragraph.
   - `src/cv-linkedin.md` — LinkedIn format: About, Experience, Education, Skills, Publications sections. Dense, formatted for copy-paste into LinkedIn.

5. **Keep the front matter** — Every page must keep its YAML front matter (layout, title, description, variant). Update `title` and `description` if the content warrants it.

6. **Build** — Run `npm run build` and confirm it completes without errors.

7. **Commit and push** — Stage all changed files, commit with a descriptive message, and push to the current branch.

---

## Known Baseline

### Career (roles)
- **Appnovation Technologies** — Technology Senior Associate (current; details in content/ if available)
- **Serti** — Senior Drupal Developer & Consultant (details in content/ if available)
- **Agence Webdiffusion** — Co-Founder & Web Architect, 2013+
- **Floe Design + Technologies** — Senior Drupal Developer / Technical Lead, 2009+
- **Freelance** — web development, 2009+

### Education
- Institut d'Urbanisme de Paris / Université Paris I Panthéon-Sorbonne — Master's, Urban Planning (thesis on morphology of emergence)
- Concordia University — B.Sc., Economics and Computer Science

### Known articles at The Nature of Cities
These are confirmed. Any new ones found in searches should be added:

1. A Fractal Solution to Regional Complexity and Governance — Jan 2020 — https://www.thenatureofcities.com/TNOC/2020/01/23/a-fractal-solution-to-regional-complexity-and-governance/
2. Neighborhoods that Change in Non-linear Ways — Jul 2019 — https://www.thenatureofcities.com/TNOC/2019/07/10/neighborhoods-that-change-in-non-linear-ways-urban-planning-for-succession/
3. Neural Networks — A New Model for 'The Kind of Problem a City Is' — Apr 2018 — https://www.thenatureofcities.com/2018/04/29/neural-networks-new-model-kind-problem-city/
4. The Effect of Iteration on Urban Form, Part II — Jun 2017 — https://www.thenatureofcities.com/2017/06/28/effect-iteration-urban-form-part-ii-iteration-ecosystem/
5. The Effect of Iteration on Urban Form, Part I — Jun 2017 — https://www.thenatureofcities.com/2017/06/25/effect-iteration-urban-form-part/
6. Uses and Abuses of Preservation — Nov 2016 — https://www.thenatureofcities.com/2016/11/13/uses-and-abuses-of-preservation/
7. Common Threads: Jane Jacobs and Elinor Ostrom — May 2016 — https://www.thenatureofcities.com/TNOC/2016/05/28/common-threads-connections-among-the-ideas-of-jane-jacobs-and-elinor-ostrom-and-their-relevance-to-urban-socio-ecology/
8. Neighborhoods and Urban Fractals — Oct 2012 — https://www.thenatureofcities.com/2012/10/17/neighborhoods-and-urban-fractals-the-building-blocks-of-sustainable-cities/

### Other writing
- Emergent Urbanism blog — http://emergenturbanism.com (since 2007)
- Medium: "Lean Drupal Development", "Peter Thiel's Zero to One"
- SlideShare: https://www.slideshare.net/mhelie
- TNOC roundtable "Read this!" Dec 2016 (book rec: Delirious New York by Rem Koolhaas)

### Links
- GitHub: https://github.com/mathieuhelie
- LinkedIn: https://www.linkedin.com/in/mhelie
- Twitter: https://twitter.com/mathieuhelie
- Email: mthl@mthl.info

---

## Style Guidelines

- **Tone**: Professional but personal. Not a stiff résumé. Conversational where appropriate.
- **Headers**: Use `##` for sections, `###` for roles/articles, `####` for org/date metadata lines
- **Dates on h4**: Use italics-in-em style: e.g., `#### Montreal, Canada | 2013–2018`
- **Links**: All TNOC article titles should be hyperlinks to their canonical URLs
- **No placeholders**: Don't write `[date TBD]` — omit dates rather than guess. Content/ docs will have more detail.
- **index.md length**: Aim for comprehensive. More detail is better for SEO. 600–1200 words of body content.
- **cv-tech.md length**: Concise. 300–500 words. Employer/recruiter audience.
- **cv-urban.md length**: Article-heavy. Lead with writing. 400–600 words.
- **cv-linkedin.md length**: Structured for copy-paste. 300–500 words. Use `---` dividers between experiences.
