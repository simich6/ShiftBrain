# ShiftBrain v0.11 — GitHub Pages prototype

A static, browser-only prototype for evidence-first troubleshooting of lyophilizers and sterile pharmaceutical manufacturing equipment.

## Run it on GitHub Pages

1. Create a GitHub repository, for example `shiftbrain`.
2. Upload `index.html` and this `README.md` to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the `main` branch and `/(root)`, then save.
6. Wait for GitHub Pages to publish the site. The URL will be shown in the Pages settings.

No build step, package manager, API key, or backend is required.

## What this prototype does

- Guided, rules-based troubleshooting for five illustrative failure modes.
- Candidate ranking based on heuristic scores.
- Free-text observations during an investigation.
- Knowledge-base browsing and local case records.
- Export of investigation reports, case lists, and workspace JSON.
- Browser-local persistence using `localStorage`.

## Important limitations

- This version does **not** connect to an LLM, external knowledge retrieval, equipment historian, MES, or CMMS.
- The initial cases and dashboard data are illustrative sample data, not verified plant history.
- The relative ranking scores are **not probabilities**, validated confidence values, or proof of root cause.
- `localStorage` is confined to one browser profile/device. It is not a shared database, controlled audit trail, or GMP-compliant record system. Clearing browser data can remove records; export backups regularly.
- Do not upload confidential, personal, product, batch, or proprietary GxP information to a public repository. GitHub Pages content in a public repository may be publicly accessible.
- This prototype is not validated for GMP use and must not replace approved procedures, qualified engineering judgment, deviation/CAPA systems, or quality-unit decisions.

## Recommended next development increment

1. Extract the diagnostic logic from the HTML into a separate module.
2. Add structured `Case`, `Hypothesis`, `Evidence`, `Test`, `Source`, and `Decision` records.
3. Record provenance and timestamps for observations and sources.
4. Replace misleading percentage-style ranking with clearly labelled heuristic scores.
5. Add test fixtures and regression tests before integrating an LLM or RAG.

## License

No license is included. Add a license explicitly if you want to grant others permission to reuse or distribute this code.
