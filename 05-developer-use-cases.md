# Domain 5 - Developer Use Cases for AI (13%)

> Where Copilot adds the most value across the SDLC.

## The eight high-value use cases

| Use case | Surface | Win |
|---|---|---|
| 1. **Boilerplate generation** | Completions | CRUD scaffolds, repetitive shapes |
| 2. **Refactoring** | Edits / Chat | Rename, extract, modernize patterns |
| 3. **Debugging** | Chat (`/fix`) | Stack-trace analysis + minimal fix |
| 4. **Documentation** | Chat (`/doc`) | Docstrings, JSDoc, README sections |
| 5. **Code translation** | Chat | Python to Java, JS to TS, etc. |
| 6. **Test scaffolding** | Chat (`/tests`) | Unit + edge cases |
| 7. **Code review prep** | PR summaries | Self-review before pushing |
| 8. **Learning new APIs** | Chat (`/explain`) | Surface idiomatic patterns |

## Boilerplate generation

```python
# Pydantic model for a Post with id, title, body, author_id
# Create POST /posts endpoint in FastAPI that validates and stores in Postgres
```
Copilot generates 60-80% complete; you tweak the rest. Best for: CRUD endpoints, DTOs, form components, config blobs.

## Refactoring

- **Rename + restructure** - select code, `/fix improve readability` or `Convert this to use async/await`.
- **Modernize** - "Convert from class component to functional with hooks".
- **Extract** - "Extract the validation logic into a separate function in #file:validators.ts".
- **Cross-file** - use **Copilot Edits** with multiple files in working set.

## Debugging

```
@workspace I get TypeError: cannot read property 'map' of undefined
in #file:Cart.tsx line 42 when checkout button clicked.
```

Tactics:
- Paste full stack trace.
- Reference the failing file.
- Provide a minimal reproduction (input + expected output).
- Use `/fix` slash command on the highlighted line.

## Documentation

- `/doc` on a function generates docstring.
- "Generate a README section explaining how to run this project locally" with `@workspace`.
- Auto-generate API reference from JSDoc with Copilot's help.

## Code translation

| From | To | Common asks |
|---|---|---|
| Python | TypeScript | Convert classes, type hints to interfaces |
| JavaScript | TypeScript | Add types, replace `any` |
| Java | Kotlin | Modernize an Android module |
| C# | F# | Refactor to functional style |
| SQL | LINQ / SQLAlchemy | ORM migration |

Caveat: always test the output. Idioms differ; sometimes Copilot translates word-for-word and produces non-idiomatic code.

## Test scaffolding

`/tests` on a function generates a test file with:
- Happy path.
- Boundary conditions.
- Invalid input handling.
- Mocked dependencies (when imports are visible).

Iterate: "Add a test for the case where the user has no orders".

## Code review prep

- **Copilot for pull requests** auto-generates the description from the diff.
- Use `/explain` on each diff hunk to validate your own change.
- Run `gh copilot review` for AI-assisted review (preview).

## Learning new APIs / frameworks

- `@workspace what's the Stripe API for refunds?`
- "Explain how React Server Components differ from Server-Side Rendering, with code examples."
- Copilot's training cutoff means latest releases may be missing - check release notes.

## SDLC integration

```mermaid
flowchart LR
    Plan[Plan: Workspace generates spec]
    Plan --> Code[Code: completions + edits]
    Code --> Test[Test: /tests + edge cases]
    Test --> Review[Review: PR summaries + /explain]
    Review --> Deploy[Deploy: gh copilot suggest CLI commands]
    Deploy --> Monitor[Monitor: explain logs + write KQL]
```

## Worked examples

- **Onboarding to a new repo**: `@workspace explain the architecture of this repo` then "where would I add a new endpoint?"
- **Migrating Express to Fastify**: open the route file, `Convert this Express route to Fastify keeping behavior identical`. Iterate file by file.
- **Filling a sparse test suite**: `/tests` on every public function in `src/utils/`, then review and prune.

## Top gotchas

1. **Copilot is not a senior engineer** - it lacks system-level understanding; verify designs.
2. **Translation can be literal** - sometimes `for` loops in Python become `for` loops in JS instead of `.map()`.
3. **Generated tests can be tautological** - they may test that the implementation does what the implementation does. Add behavioral assertions.
4. **Hallucinated APIs** - a "translated" snippet may reference a method that doesn't exist in the target language.
5. **Refactor scope creep** - Copilot may rewrite more than asked. Use Copilot Edits to scope.
6. **Documentation drift** - regenerated docs can lose nuance; review.

## References

- [Common use cases for GitHub Copilot](https://docs.github.com/copilot/using-github-copilot/example-use-cases-for-github-copilot)
- [Refactoring with Copilot Chat](https://docs.github.com/copilot/copilot-chat-cookbook/refactoring-code)

---

[Domain 4](04-prompt-crafting.md) - [Domain 6: Testing with Copilot](06-testing-with-copilot.md)
