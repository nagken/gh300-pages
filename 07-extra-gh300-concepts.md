# GH-300 Extra Concepts (Beyond the Skills Outline)

> Subtle nuances that show up in tricky exam wording.

## Copilot Chat participants

| Participant | Scope |
|---|---|
| `@workspace` | Whole workspace, semantic-searched |
| `@terminal` | Last terminal output |
| `@vscode` | VS Code features and commands |
| `@github` | Search across GitHub.com (Enterprise) |

## Copilot Edits vs Workspace

| Aspect | Edits | Workspace |
|---|---|---|
| Surface | IDE | Web (github.com) |
| Output | Direct file diffs you accept | Spec then plan then implementation then PR |
| Plans | All paid | Enterprise (preview) |
| Best for | Targeted multi-file change | Full feature with PR |

## Public code filter threshold

- Approximately **150 characters** of contiguous match against public GitHub code triggers the filter.
- Three settings: **Block** / **Allow** / **Allow with citation**.

## Suggestion data flow nuances

- Code is sent **transient** for inference; not stored beyond the request for Business / Enterprise.
- For Free / Pro / Pro+, snippets may be retained up to **28 days** for abuse / safety review.
- **Embeddings for `@workspace`** in VS Code are computed locally - they do not leave the IDE.

## Rate limits / fair-use

- Free: 2k completions, 50 chat / month.
- Paid plans: high but not literally infinite - egregious automated abuse can be throttled.
- Premium models (Pro+, Enterprise) may have separate per-minute caps shown in the model picker.

## IDE policy cascade

```
Personal account default
  -> Org policy (Business / Enterprise)
    -> Repo-level content exclusion (Business / Enterprise)
      -> Effective behavior in IDE
```

## GHE Server vs GHE Cloud

- Copilot is supported on **GHE Cloud** (with EMU possible).
- Copilot is NOT a feature of **GHE Server** as a self-hosted product. GHE Server users access Copilot through their GitHub.com account (with allowed network egress).

## Telemetry granularity

- "Suggestion **shown**" = displayed as ghost text.
- "Suggestion **accepted**" = developer pressed Tab.
- Acceptance % = a productivity proxy, not a quality metric.

## Slash command nuances

- `/explain` works on selection or whole file.
- `/fix` may rewrite the function entirely - inspect.
- `/tests` requires understanding of the test framework in the repo (open a sibling `*.test.ts` first).
- `/doc` follows the language's idiomatic doc style (PEP-257, JSDoc, XMLDoc).

## Copilot in CLI specifics

- `gh copilot suggest` interactive: walks you through goal then shell type then revision then execution.
- `gh copilot explain "<cmd>"` no execution; just explanation.
- Requires `gh` CLI authenticated; subject to your org's Copilot CLI policy.

## Knowledge base specifics

- Sourced from one or many GitHub repos containing Markdown / docs.
- Indexed and queried via Chat with `@workspace` against the kb.
- Updates require re-indexing (manual trigger or schedule).
- Enterprise-only.

## Custom models

- Limited preview. Fine-tune a Copilot model on your private repos.
- Requires significant code volume + GitHub-managed training pipeline.
- Helps suggestions match house conventions / private APIs.

## Spaces (Copilot)

- Curated context bundles for Chat (web) - pin code, docs, links.
- Beta / Enterprise feature.

## Audit log gotchas

- Events use `copilot.*` actor / action.
- Limited retention on Business plan; longer on Enterprise.
- API access is enterprise-grade; UI filtering is similar to standard audit.

---

[Master Index](00-MASTER-INDEX.md)
