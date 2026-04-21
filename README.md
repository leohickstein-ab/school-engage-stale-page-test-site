# school-engage-stale-page-test-site

Disposable static site for stale-page cleanup testing from `dev-leo`.

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
