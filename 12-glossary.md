# GH-300 Glossary

| Term | Meaning |
|---|---|
| **Audit log** | Record of admin and Copilot events at org / enterprise level |
| **Business (Copilot)** | Mid-tier plan with IP indemnity + admin controls + content exclusions |
| **Chat (Copilot)** | Conversational interface inside the IDE or web with code awareness |
| **Code completion** | Inline ghost-text suggestion shown as you type |
| **Completion model** | The fast LLM optimized for low-latency inline suggestions |
| **Content exclusion** | Org / repo-level glob pattern preventing Copilot from reading matching files |
| **Context window** | Maximum tokens the model can attend to in one request |
| **Custom model** | Enterprise-only fine-tune of Copilot on private code |
| **Edits (Copilot)** | Multi-file natural-language driven diffs with accept/reject UI |
| **Enterprise (Copilot)** | Top-tier plan adding knowledge bases + custom models + Spaces |
| **Free (Copilot)** | Capped plan: 2k completions + 50 chat msgs / month |
| **Ghost text** | The grey inline suggestion text from completions |
| **GitHub Skills** | Free interactive courses on github.com |
| **gh copilot** | CLI subcommand with `suggest` and `explain` |
| **Hallucination** | Confident but factually wrong model output |
| **IP indemnity** | GitHub's commitment to defend against IP claims arising from accepted suggestions |
| **JIT context** | Files / selections / terminal output added to a chat prompt on demand |
| **Knowledge base** | Enterprise feature - curated repo content queryable via Chat |
| **LLM** | Large Language Model (GPT-4o, Claude 3.5, Gemini, etc.) |
| **Model picker** | UI letting users select among allowed LLMs |
| **OAuth scope** | Permission set granted to Copilot extension in IDE |
| **Pro (Copilot)** | Individual paid plan; unlimited completions + chat |
| **Pro+ (Copilot)** | Pro plus access to premium models |
| **Prompt** | The text + context sent to the model |
| **Public code filter** | Filter that blocks suggestions matching ~150+ chars of public GitHub code |
| **Pull request summary** | Auto-generated description of a PR diff |
| **Reference output** | Suggestion shown with citation to matching public code |
| **SAML / SSO** | Org-level authentication; Business / Enterprise feature |
| **SCIM** | Automated user provisioning; Business / Enterprise feature |
| **Slash command** | Chat shortcut like `/explain`, `/fix`, `/tests` |
| **Spaces (Copilot)** | Curated context bundle for Chat (web) - Enterprise preview |
| **Telemetry** | Anonymized usage events sent to GitHub for ops + improvement |
| **Token** | Unit of text used by LLMs (~ a word or sub-word) |
| **Toxicity filter** | Filter blocking offensive / harmful content in Chat output |
| **Training opt-in** | Allow GitHub to use your code snippets to train Copilot |
| **Vulnerability filter** | Lightweight check for common insecure patterns in suggestions |
| **Workspace (Copilot)** | Spec / plan / implementation / PR mode (Enterprise web) |
| **`@github`** | Chat participant for searching across GitHub |
| **`@terminal`** | Chat participant referencing terminal output |
| **`@vscode`** | Chat participant for VS Code feature questions |
| **`@workspace`** | Chat participant for semantic search across the workspace |
| **`#file`** | Chat reference - include this specific file |
| **`#selection`** | Chat reference - include the current selection |

---

[Master Index](00-MASTER-INDEX.md)
