# LiNKsites Factory Kit

Factory-style workspace for generating many SMB websites from reusable templates, backed by a centralized Payload CMS.

Previously named: "Dev_Sites Website Factory".

## Structure

```
Dev_Sites/ (workspace root)
├── library/               # Central documentation library (SOPs, runbooks, env matrix)
├── sites_specs/           # Authoritative specifications (system + architectures)
├── sites_cms/             # Central CMS (Payload CMS) for all sites
│   └── payload-cms/       # Payload app (Next.js + Payload)
├── sites_templates/       # Templates and shared template assets
│   ├── website-master-template/  # Primary Next.js template (starting point)
│   ├── company-site/      # Smaller starter template
│   └── shared/            # Shared assets/snippets
└── sites_projects/        # Experiments / older project copies (not the primary path)
```

## Usage

- The CMS lives in `sites_cms/payload-cms` and stores content for all sites.
- Website templates live in `sites_templates/`.
- Sites are served in two modes:
  - Shared platform mode (many sites on one running Next.js platform, by hostname).
  - Premium spin-off mode (dedicated frontend deployment per site, still using the central CMS by `siteId`).

## Documentation Library (Primary Entry Point)

Use the central documentation library first:

- `/Users/linktrend/Projects/Dev_Sites/library/README.md`

The library includes:
- workflow and architecture references
- implementation and operations SOPs
- environment matrix and runbooks
- business/pricing SOPs
- links to source specs and active code repositories

## Legacy Top-Level Docs

These are still valid and linked from the library:
- `LINKSITES_FACTORY_KIT_WORKFLOW.md`
- `IMPLEMENTATION_PLAN.md`
- `APPROACH_EVALUATION.md`
- `TEMPLATE_CREATION_GUIDE.md`
- `LINKSITES_FACTORY_ARCHITECTURE.md`
- `VPS_DEPLOYMENT_GUIDE.md`
- `GODADDY_DNS_SETUP.md`
- `SUPABASE_SETUP.md`
