# GH-300 Pitfalls and Gotchas

> Wrong-answer traps the exam loves to set.

## 1. `.gitignore` does NOT block Copilot

A file in `.gitignore` is still on disk and still readable by your IDE - and therefore by Copilot. Use **content exclusions** (Business / Enterprise) to truly block.

## 2. Public code filter is OFF by default for personal plans

Pro / Pro+ users start with the filter OFF. Orgs typically force it ON via policy.

## 3. IP indemnity starts at Business

Pro and Pro+ have no indemnity. If the question mentions "GitHub will defend customers against IP claims," the answer is Business or Enterprise.

## 4. Knowledge bases are Enterprise-only

Business plan does NOT include knowledge bases. Question mentioning "ground answers in our internal documentation" implies Enterprise.

## 5. Custom / fine-tuned models are Enterprise (preview)

Pro+ does not give you custom models despite having premium-model access.

## 6. Content exclusions are NOT retroactive

Past chat history does not get scrubbed. New context after exclusion is set will respect it.

## 7. Personal plans default to OPT-IN for training

Many candidates assume opt-out by default. It's the opposite for Free / Pro / Pro+.

## 8. Audit logs are limited on Business

Full audit log API is Enterprise-grade. Business shows policy + seat events but limited Chat-level audit.

## 9. `/fix` may rewrite the test, not the bug

When a test fails, `/fix` might patch the test instead of the implementation. Inspect the diff.

## 10. Generated tests can be tautological

Copilot's `/tests` may assert that the implementation does what the implementation does. Add behavioral assertions.

## 11. `@workspace` is semantic search, not a chat memory

It re-runs an embedding lookup per query. It is local to your IDE for VS Code.

## 12. Free plan caps reset monthly, not weekly or daily

2,000 completions and 50 chat messages **per month**.

## 13. Verified students get Pro free, not Pro+

Pro+ is paid for everyone.

## 14. SAML SSO is Business / Enterprise

Personal plans do not enforce org SAML.

## 15. Hallucinated APIs

Copilot can confidently propose `pandas.DataFrame.write_excel()` which doesn't exist. Always run / test.

## 16. Premium model access varies by plan

Pro+ unlocks broader premium-model access; Business covers standard models; Enterprise broadens to custom + Spaces. Don't conflate "all plans get Claude" - it depends on policy.

## 17. Spaces (Copilot Spaces) is web-only

Don't expect a Spaces button in VS Code IDE.

## 18. PHI / HIPAA

GitHub does NOT sign a BAA for Copilot. Don't paste PHI into prompts even on Enterprise.

---

[Master Index](00-MASTER-INDEX.md)
