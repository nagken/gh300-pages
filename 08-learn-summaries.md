# GH-300 Learn Summaries

> Microsoft Learn / GitHub docs paragraph summaries grouped by domain.

## Domain 1 - Responsible AI

**Responsible use of GitHub Copilot.** Covers limitations of LLMs - hallucinations, bias, security flaws, license risk. Mitigations: public code filter, vulnerability filter, toxicity filter on Chat. Emphasizes user accountability: review every suggestion, run tests + SAST + license scanners. Org-level controls amplify safety: content exclusions, mandatory public-code-filter ON, audit logs.

## Domain 2 - Plans and Features

**Plans for GitHub Copilot.** Five tiers: Free (capped), Pro, Pro+, Business, Enterprise. IP indemnity + content exclusions begin at Business; knowledge bases + custom models are Enterprise-only. Free students and verified open-source maintainers receive Pro free. Plans differ in seat-management, model-selection policy, audit logging, and access to premium models.

**Copilot features.** Code completions (low-latency ghost text), Copilot Chat (panel + inline), Copilot Edits (multi-file diffs), Copilot Workspace (spec/plan/PR for Enterprise web), Copilot in CLI (`gh copilot`), Copilot in pull requests (auto-summary), knowledge bases (Enterprise grounded retrieval), custom models (Enterprise fine-tune).

## Domain 3 - How It Works

**How GitHub Copilot processes data.** Prompt = current file + nearby tabs + selection + chat history (where applicable). Sent over TLS to GitHub proxy, filtered, forwarded to LLM provider, response filtered (public code match, toxicity), returned. Files in `.gitignore` are NOT excluded automatically; use **content exclusions** for true blocking.

**Managing Copilot.** Org / Enterprise admin sets policy: model allow-list, public-code-filter mode, content exclusion paths, IDE chat surface toggles, telemetry / training opt-out. Audit log surfaces `copilot.*` events: seat changes, policy changes, content-exclusion modifications.

## Domain 4 - Prompt Crafting

**Prompt engineering for Copilot.** Be specific, provide context (open relevant files, use `#file:` and `@workspace`), show examples, iterate. Use slash commands (`/explain`, `/fix`, `/tests`, `/doc`, `/optimize`). Cursor position + filename + recent edits are all part of the implicit prompt. Anti-pattern: vague verbs ("make it better"); fix by stating axis (faster, shorter, more readable).

## Domain 5 - Developer Use Cases

**Use cases.** Boilerplate (CRUD, DTOs), refactoring (rename, modernize, extract), debugging (`/fix` with stack trace), documentation (`/doc`), code translation (Python to TS), test scaffolding (`/tests`), code review prep (PR summaries), learning new APIs (`/explain`). Copilot integrates across the SDLC: plan (Workspace) then code (completions / edits) then test (`/tests`) then review (PR summaries) then deploy (CLI).

## Domain 6 - Testing with Copilot

**Generating tests.** `/tests` scaffolds happy-path tests; ask explicitly for edge cases, error conditions, mocked dependencies. Copilot infers test framework from existing test files in the repo - open one before prompting. TDD with Copilot: write failing test, ask Copilot to implement minimum code to pass, refactor with Edits. Risks: tautological tests, flaky tests, snapshot pass-on-first-run, low-value coverage padding.

## Domain 7 - Privacy

**Privacy and content exclusions.** Personal plans default OPT-IN to using your code as training data; Business / Enterprise default OPT-OUT. Content exclusions (Business / Enterprise only) accept glob patterns at org or repo level; matching files are not read by Copilot for completions or chat. Public code filter blocks ~150+ char verbatim matches against public GitHub code (default OFF for personal; recommended ON for orgs). No HIPAA BAA for Copilot - keep PHI out of prompts.

---

[Master Index](00-MASTER-INDEX.md)
