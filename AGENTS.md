# Vaultix Gate website

Static bilingual (EN/ES) marketing site. English pages at root, Spanish under `es/`.

## Deploy to local XAMPP

The live local copy is served from `C:\xampp\htdocs\vaultixlabs.github.io`.
To sync the repo to it, run (PowerShell — Git Bash mangles the `/` flags):

```powershell
robocopy "C:\Users\rodmo\OneDrive\vaultixlabs.github.io" "C:\xampp\htdocs\vaultixlabs.github.io" /MIR /XD .git /NFL /NDL /NJH
```

`/MIR` mirrors the tree (deletes extras in destination). Robocopy exit codes 0–7 are success.

Trigger: when the user says "publica vaultix web" / "deploy vaultix site", run the command above. This trigger is specific to the Vaultix Gate website deploy only.

## Conventions

- Shared stylesheet: `assets/css? v=N` — bump the `?v=` query in all 10 HTML files after CSS changes.
- Copy rules: expand acronyms on first use; no em-dashes in marketing copy; ES copy must be natural Spanish, not literal translation.
- ES section anchors are Spanish (`#precios-del-software`, `#integracion`); EN uses `#pricing`, `#developers`.
