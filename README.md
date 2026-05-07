# Sidecar Data Docs

Customer-facing documentation for Sidecar, built with [Mintlify](https://mintlify.com).

## Setup (First Time)

1. Sign up at [mintlify.com](https://mintlify.com) and create an organization.
2. Install the [Mintlify GitHub App](https://dashboard.mintlify.com/settings/organization/github-app) and connect this repo.
3. In the Mintlify dashboard, set the docs directory to `docs/` (the subdirectory containing `docs.json`).
4. Push to the default branch — Mintlify will auto-deploy.
5. (Optional) Set up a custom domain (e.g., `docs.sidecardata.com`):
   - In the Mintlify dashboard, go to Settings > Custom Domain.
   - Add a CNAME record in your DNS provider: `docs.sidecardata.com` → `cname.mintlify.com`.
   - Mintlify handles SSL automatically.

## Local Development

Requires Node 22 (LTS). If you're on a newer version, use Docker:

```bash
docker run --rm -p 3333:3333 -v $(pwd):/app -w /app node:22-alpine sh -c "npx -y mintlify dev --host 0.0.0.0 --port 3333"
```

Preview at `http://localhost:3333`.

## Deployment

Changes pushed to the default branch are automatically deployed via the [Mintlify GitHub App](https://dashboard.mintlify.com/settings/organization/github-app). Pull requests get preview deployments.

## Structure

```
docs/
├── docs.json                          # Mintlify config (nav, theme, branding)
├── index.mdx                          # Landing page
├── quickstart.mdx                     # Quickstart guide
└── integrations/
    ├── data-warehouses/               # Snowflake, BigQuery, Redshift, Databricks
    ├── transformation/                # dbt Cloud, dbt Core
    ├── bi-analytics/                  # Looker, Metabase, Lightdash, Omni, Power BI
    ├── extract-load/                  # Fivetran
    ├── communication/                 # Slack, Microsoft Teams
    ├── project-management/            # Jira, Linear
    └── other/                         # Sidecar MCP, Contract Agent
```

## Screenshots

<img width="2438" height="1433" alt="image" src="https://github.com/user-attachments/assets/0fc7a120-f844-40e4-9fdc-4742c2f5dd98" />

<img width="2296" height="1439" alt="image" src="https://github.com/user-attachments/assets/8c11ee7f-35e9-43c7-bff2-d792ed047528" />


