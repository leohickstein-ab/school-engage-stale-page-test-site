# school-engage-stale-page-test-site

Disposable static site for controlled RAG retrieval quality testing from `dev-leo`.

Published URL:

- `https://leohickstein-ab.github.io/school-engage-stale-page-test-site/`

Why this repo exists:

- Gives `dev-leo` a public website to crawl
- Provides deterministic public, agent-facing, internal-only, and PDF-only facts for RAG comparison

Controlled RAG fixture pages:

- `program-a.html`: Northern Lakes Aviation Maintenance, code `NLA-240`, Hangar Bay Campus, 24 months
- `program-b.html`: Digital Health Records Certificate, code `DHR-118`, Lakeside Health Campus, 8 months
- `student-services.html`: Student Success Centre, room `L210`, Blue Heron Emergency Bursary
- `agent-resources.html`: agent-only reference code `AGENT-BLUE-42`
- `internal-advisor-notes.html`: internal-only keyword `MAPLE-VAULT-73`
- `rag-fixture-handbook.pdf`: PDF-only facts `PDF-9001`, `555-0199`, and `Cedar Hall C301`
- `/faq/`: exact path exclusion fixture, token `FAQ-EXCLUSION-2026`
- `/faq-old/`: non-matching control for `/faq`, token `FAQ-OLD-CONTROL-2026`
- `/blog/`: blog keyword root fixture, token `BLOG-ROOT-2026`
- `/blog/article-1/`: nested blog keyword fixture, token `BLOG-ARTICLE-2026`
- `/news/`: news keyword root fixture, token `NEWS-ROOT-2026`
- `/news/story-1/`: nested news keyword fixture, token `NEWS-STORY-2026`
- `/programs/business/`: non-excluded control fixture, token `BUSINESS-CONTROL-2026`

Exclusion rule test cases:

1. Add the full URL ending in `/faq/`; the UI should display `/faq` or `/faq/` as the path tag and preview one affected page.
2. Excluding `/faq` should not exclude `/faq-old/`.
3. The Blog preset should exclude `/blog/` and `/blog/article-1/`.
4. The News preset should exclude `/news/` and `/news/story-1/`.
5. `/programs/business/` should remain indexed while FAQ, Blog, and News exclusions are tested.

Suggested comparison queries:

1. What is the program code for Northern Lakes Aviation Maintenance?
2. Which campus offers the Digital Health Records Certificate?
3. What services are available at the Student Success Centre?
4. What is the partner portal reference code for agents?
5. What is the advisor-only scholarship keyword?
6. What is the document code in the RAG fixture handbook PDF?
7. What is the PDF-only orientation room?
