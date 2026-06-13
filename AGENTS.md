# ISAB repository instructions

## Standing rules

- Use the name `ISAB` exactly.
- Treat GitHub as the durable source of truth.
- Do not rely on Codex chat history as the only place where a fact, decision, deployment state, or next step exists.
- Start nontrivial work from a GitHub issue.
- End nontrivial work with a durable handoff in the issue, PR, docs, or `CODEX_COORDINATION.md`.
- Never commit secrets, tokens, cookies, private keys, OAuth artifacts, local credential caches, one-time codes, or raw Codex transcripts.
- Prefer small, reviewable changes.
- Prefer branch and pull request for nontrivial changes.
- Do not deploy unless deployment is explicitly in scope.
- If shared Azure SQL schema, Microsoft Entra groups, Cloudflare routes, DNS, public hostnames, or auth policy are touched, update `CODEX_COORDINATION.md` and the ISAB control-plane repo.

## Before work

Read:

- `README.md`
- `AGENTS.md`
- `CODEX_COORDINATION.md`, if present
- relevant files under `docs/`
- the GitHub issue defining the task

## Genomic Hit Locator rules

- This is a public research tool linked to ISAB infrastructure.
- Keep uploaded scientific data, sample data, and local private paths out of Git unless intentionally public and sanitized.
- Preserve user-facing README accuracy because the app renders the README at `/readme`.
- Keep deployment and hostname assumptions coordinated with the ISAB edge repo.

## Before stopping

Record:

- summary
- files changed
- checks run
- deployment state
- assumptions changed
- next action

## Review guidelines

- Treat committed secrets as P0.
- Treat raw Codex transcript dumps as P0.
- Treat production auth, DNS, SQL, Entra, Cloudflare, or Azure changes without explicit issue scope as P0.
- Treat missing documentation for changed cross-repo assumptions as P1.
