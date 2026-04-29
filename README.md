# school-engage-stale-page-test-site

Disposable static site for stale-page cleanup and RAG retrieval quality testing from `dev-leo`.

Published URL:

- `https://leohickstein-ab.github.io/school-engage-stale-page-test-site/`

Common test scenarios:

1. Disappeared page:
   - Remove the `old-page.html` link from `index.html`
   - Remove the `old-page.html` entry from `sitemap.xml`
   - Keep `old-page.html` on disk

2. `404` page:
   - Keep the link in `index.html` and `sitemap.xml`
   - Rename or delete the actual file, for example `program-b.html`

3. Restore:
   - Re-add the file and sitemap/homepage references

Why this repo exists:

- Gives `dev-leo` a public website to crawl
- Lets stale-page cleanup be tested without depending on localhost
- Provides deterministic public, agent-facing, and internal-only facts for RAG comparison

Controlled RAG fixture pages:

- `program-a.html`: Northern Lakes Aviation Maintenance, code `NLA-240`, Hangar Bay Campus, 24 months
- `program-b.html`: Digital Health Records Certificate, code `DHR-118`, Lakeside Health Campus, 8 months
- `student-services.html`: Student Success Centre, room `L210`, Blue Heron Emergency Bursary
- `agent-resources.html`: agent-only reference code `AGENT-BLUE-42`
- `internal-advisor-notes.html`: internal-only keyword `MAPLE-VAULT-73`
- `rag-fixture-handbook.pdf`: PDF-only facts `PDF-9001`, `555-0199`, and `Cedar Hall C301`

Suggested comparison queries:

1. What is the program code for Northern Lakes Aviation Maintenance?
2. Which campus offers the Digital Health Records Certificate?
3. What services are available at the Student Success Centre?
4. What is the partner portal reference code for agents?
5. What is the advisor-only scholarship keyword?
6. What is the document code in the RAG fixture handbook PDF?
7. What is the PDF-only orientation room?
