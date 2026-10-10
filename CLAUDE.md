# constructionleads-runner
PUBLIC repo that runs the PRIVATE empireofryan/ConstructionLeads daily permit report (Phoenix) on free public-repo Actions minutes.
- Workflow checks out the private repo with secret CL_DEPLOY_KEY (write deploy key on ConstructionLeads only), runs ingest-phoenix + daily-report, pushes reports/ back. Output kept out of public logs.
- Secrets: CL_DEPLOY_KEY, DATABASE_URL. Cron 12:00 UTC (5am Phoenix). Manual: `gh workflow run daily-report.yml -R empireofryan/constructionleads-runner`
- The private repo's own daily-report workflow is disabled_manually (private minutes exhausted). Verified working 2026-10-10.
