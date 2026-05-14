# GH-300 Flashcards

> Interactive flashcards. Click to flip. Topics organized by exam domain.

<section class="fc-section" data-fc-title="Responsible AI">

<div class="flashcard">
<div class="fc-q">What does the public code matching filter do?
<div class="fc-a"><strong>Blocks (or cites) suggestions whose ~150+ contiguous characters match public code on GitHub.</strong> Default OFF for personal plans; recommended ON for orgs.</div>
</div>
</div>

<div class="flashcard">
<div class="fc-q">Three risks of LLM-generated code?
<div class="fc-a"><strong>Hallucinated APIs, security vulnerabilities (e.g. SQL injection), license-incompatible matches.</strong></div>
</div>
</div>

<div class="flashcard">
<div class="fc-q">Who is accountable for Copilot suggestions you accept?
<div class="fc-a"><strong>You</strong> (and your org). Copilot is an assistant; review every suggestion.</div>
</div>
</div>

</section>

<section class="fc-section" data-fc-title="Plans and Features">

<div class="flashcard">
<div class="fc-q">Caps on Copilot Free?
<div class="fc-a"><strong>2,000 completions and 50 chat messages per month.</strong></div>
</div>
</div>

<div class="flashcard">
<div class="fc-q">Lowest plan with IP indemnity?
<div class="fc-a"><strong>Copilot Business.</strong> Pro and Pro+ do NOT include indemnity.</div>
</div>
</div>

<div class="flashcard">
<div class="fc-q">Plans with content exclusions?
<div class="fc-a"><strong>Business and Enterprise only.</strong> Personal plans cannot path-block.</div>
</div>
</div>

<div class="flashcard">
<div class="fc-q">Plan required for knowledge bases?
<div class="fc-a"><strong>Enterprise only.</strong> Business does not include them.</div>
</div>
</div>

<div class="flashcard">
<div class="fc-q">Plan required for custom (fine-tuned) models?
<div class="fc-a"><strong>Enterprise (limited preview).</strong></div>
</div>
</div>

<div class="flashcard">
<div class="fc-q">Difference between Copilot Edits and Copilot Workspace?
<div class="fc-a"><strong>Edits</strong>: multi-file IDE diffs. <strong>Workspace</strong>: spec then plan then implementation then PR on GitHub.com (Enterprise preview).</div>
</div>
</div>

</section>

<section class="fc-section" data-fc-title="How It Works and Management">

<div class="flashcard">
<div class="fc-q">Does `.gitignore` block Copilot from reading a file?
<div class="fc-a"><strong>No.</strong> Use <strong>content exclusions</strong> (Business / Enterprise) for that.</div>
</div>
</div>

<div class="flashcard">
<div class="fc-q">Default training-data setting on personal plans?
<div class="fc-a"><strong>Opt-IN by default.</strong> You must flip the toggle to opt out.</div>
</div>
</div>

<div class="flashcard">
<div class="fc-q">Default training-data setting on Business / Enterprise?
<div class="fc-a"><strong>Opt-OUT by default.</strong> Code is not used to train.</div>
</div>
</div>

<div class="flashcard">
<div class="fc-q">Where do you set the model allow-list for an org?
<div class="fc-a"><strong>Org / Enterprise admin then Copilot then Policies then Models.</strong></div>
</div>
</div>

<div class="flashcard">
<div class="fc-q">Audit log event prefix for Copilot?
<div class="fc-a"><strong>`copilot.*`</strong> e.g. `copilot.policy_create`, `copilot.cfb_seat_assigned`.</div>
</div>
</div>

</section>

<section class="fc-section" data-fc-title="Prompt Crafting">

<div class="flashcard">
<div class="fc-q">Four prompt-crafting principles?
<div class="fc-a"><strong>Be specific, provide context, show examples, iterate.</strong></div>
</div>
</div>

<div class="flashcard">
<div class="fc-q">Difference between `@workspace` and `#file:`?
<div class="fc-a"><strong>`@workspace`</strong> = semantic search across all files. <strong>`#file:`</strong> = explicit include of a single file.</div>
</div>
</div>

<div class="flashcard">
<div class="fc-q">Slash command to explain selected code?
<div class="fc-a"><strong>`/explain`</strong></div>
</div>
</div>

<div class="flashcard">
<div class="fc-q">Slash command to scaffold tests?
<div class="fc-a"><strong>`/tests`</strong></div>
</div>
</div>

</section>

<section class="fc-section" data-fc-title="Use Cases and Testing">

<div class="flashcard">
<div class="fc-q">Best surface for multi-file refactor?
<div class="fc-a"><strong>Copilot Edits</strong> with the relevant files in working set.</div>
</div>
</div>

<div class="flashcard">
<div class="fc-q">How does Copilot infer the test framework?
<div class="fc-a"><strong>From existing test files in the repo.</strong> Open a sibling `*.test.ts` before prompting.</div>
</div>
</div>

<div class="flashcard">
<div class="fc-q">Risk of `/fix` on a failing test?
<div class="fc-a"><strong>It may modify the test to mask the bug.</strong> Always inspect the diff.</div>
</div>
</div>

<div class="flashcard">
<div class="fc-q">CLI command to explain an opaque shell command?
<div class="fc-a"><strong>`gh copilot explain "<command>"`</strong></div>
</div>
</div>

</section>

<section class="fc-section" data-fc-title="Privacy">

<div class="flashcard">
<div class="fc-q">Does GitHub sign a HIPAA BAA for Copilot?
<div class="fc-a"><strong>No.</strong> Keep PHI out of Copilot prompts.</div>
</div>
</div>

<div class="flashcard">
<div class="fc-q">Pattern format for content exclusions?
<div class="fc-a"><strong>`.gitignore`-style globs</strong> e.g. `secrets/**`, `**/*.env`.</div>
</div>
</div>

<div class="flashcard">
<div class="fc-q">Where are exclusions configured?
<div class="fc-a"><strong>Org or repo settings then Copilot then Content exclusions.</strong> Business / Enterprise only.</div>
</div>
</div>

</section>

---

[Master Index](00-MASTER-INDEX.md)
