# ITS Wiki

Static internal wiki for **Indochina Travel Services (ITS Vietnam)** — company overview, departments, org chart, and workflow reference. Plain static HTML/CSS, no build step.

## Structure

- `index.html` — home / company overview
- `departments.html` — departments & staff directory (personal phone numbers deliberately excluded; shared hotlines and company emails only)
- `org-chart.html` — organizational hierarchy
- `workflows.html` — draft workflow reference (needs real internal process docs)
- `style.css` — shared styling (light/dark aware)

## Content status

Several sections are **drafts/placeholders** built from public info (itsvietnam.com) and an internal `organisation chart_AUG2026.xls` file, clearly marked with ⚠️ callouts. Please review and correct before treating this as authoritative.

## Local preview

No build tools needed — open `index.html` directly, or serve the folder:

```bash
python3 -m http.server 8000
```

## Deployment

Deploys automatically to **Cloudflare Pages** via GitHub Actions on every push to `main` (see `.github/workflows/deploy.yml`). Requires these GitHub repo secrets:

- `CLOUDFLARE_API_TOKEN` — API token with "Cloudflare Pages: Edit" permission
- `CLOUDFLARE_ACCOUNT_ID` — your Cloudflare account ID

See the workflow file for the exact project name used (`its-wiki`) — create a matching Cloudflare Pages project first (Dashboard → Workers & Pages → Create → Pages → Direct Upload, or let the first Action run create it).
