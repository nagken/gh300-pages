# GH-300 Hands-On Labs

> Free, browser / IDE-based exercises to internalize Copilot. Most need only a free GitHub account.

## Foundational

1. **GitHub Skills: Introduction to GitHub Copilot** - [skills.github.com](https://skills.github.com/) - guided repo walkthrough.
2. **GitHub Skills: Code with GitHub Copilot** - hands-on completions in a sample repo.
3. **Microsoft Learn: Develop with GitHub Copilot** - [learn.microsoft.com path](https://learn.microsoft.com/training/paths/copilot/) - module-based learning.

## Domain 2 - Plans and Features

4. **Try Copilot Free in VS Code** - install the GitHub Copilot extension, sign in, accept the free trial; complete a small Python script via completions.
5. **Copilot Edits sample** - clone a small Express app, ask Edits to convert it to Fastify across all files. Inspect each diff.
6. **Copilot CLI** - `gh extension install github/gh-copilot`; run `gh copilot suggest "compress all .log files older than 7 days"`.

## Domain 3 - How It Works

7. **Set a content exclusion** (requires Business / Enterprise trial) - exclude `**/*.env`; verify the IDE indicator says Copilot is disabled in `.env` files.
8. **Inspect telemetry settings** - github.com / Settings / Copilot - toggle "Allow GitHub to use my code snippets" off.
9. **Audit log walkthrough** (Business / Enterprise) - filter events by `action:copilot.*`.

## Domain 4 - Prompt Crafting

10. **Comment-driven completion** - write 3 increasingly specific comments above a function signature; observe quality progression.
11. **Slash command tour** - in any repo, run `/explain`, `/fix`, `/tests`, `/doc`, `/optimize` on the same function.
12. **`@workspace` semantic search** - ask "where do we handle authentication?" in a multi-file repo; review answers.

## Domain 5 - Use Cases

13. **Refactor with Edits** - convert a class component to a hooks-based functional component across multiple files in a React sample.
14. **Code translation** - paste a Python module; ask Copilot Chat to translate to TypeScript; manually verify.
15. **Boilerplate** - generate a FastAPI CRUD scaffold from a comment-driven prompt.

## Domain 6 - Testing

16. **Generate tests from a function** - select a `parseDate` function and run `/tests`; iterate to add edge cases.
17. **TDD with Copilot** - write a failing Vitest test for `slugify`; ask Copilot to implement; iterate to green.
18. **Mock external services** - ask Copilot to mock a `fetch` call returning a fixed response.

## Domain 7 - Privacy

19. **Set a content exclusion at repo level** (Business / Enterprise) - exclude `regulated/**`; commit a sample file there; observe block in IDE.
20. **Toggle public code filter** - personal Copilot settings; create a function that historically resembles a famous OSS snippet; observe behavior with filter on vs off.

## Putting it together

21. **End-to-end feature** - open an issue describing a small feature; use Copilot Chat for design Q&A, completions for code, Edits for cross-file changes, `/tests` for tests, PR summary for the description. Review every step.

---

[Master Index](00-MASTER-INDEX.md)
