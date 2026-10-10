# SriVerse Scholar

**One Intelligent Workspace for Learning, Teaching & Research.**

SriVerse Scholar is a local-first academic workspace designed to bring study, research, document reading, note-taking, assessment, and writing tools into one interface.

## Start here

- Open `index.html` in a modern browser, or host this repository as a static website.
- The application is a single-page HTML/CSS/JavaScript app; it does not require a Node.js build step.
- Some document readers and formatting features use third-party browser libraries loaded from CDNs, so those specific features require an internet connection.

## Privacy and storage

- User workspace data is primarily stored in the browser using IndexedDB/local browser storage.
- Browser-local data is not a cloud backup and does not automatically sync across devices. Clearing browser data may remove it; use the application's export feature for backups.
- AI generation depends on a configured external provider or a local model server. A static site cannot safely keep a private API key secret. Do not paste private provider keys into public source code.
- Source-grounded answers are only as reliable as the retrieved excerpts. Verify citations against the original document.

## Deploy

### GitHub Pages
1. Open **Settings → Pages** in this repository.
2. Select **Deploy from a branch**.
3. Choose the `main` branch and `/(root)`, then save.
4. Wait for GitHub Pages to publish the site.

### Vercel
The repository is a static HTML app. Configure the Vercel project with **Other** / no framework preset and no build command; the output should be the repository root. Confirm deployment logs before sharing the URL.

## Automated checks

GitHub Actions validates the HTML shell, parses inline JavaScript blocks, checks essential application markers, and scans for a few common hard-coded API-key patterns on pushes and pull requests. These are useful baseline checks, not a complete security audit or full browser end-to-end test.

## Development principles

- Keep core local workflows usable without a paid subscription.
- Make provider limits and unavailable features explicit.
- Never fabricate citations, source page numbers, model availability, or test results.
- Test changes before treating a feature or deployment as complete.
