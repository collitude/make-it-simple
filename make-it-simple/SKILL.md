---
name: make-it-simple
description: Take the shortest reliable path to a requested change. Use when copying or adapting an existing workflow, editing a file or configuration, fixing a specific behavior, or when the user wants a simpler approach.
metadata:
  version: "1.1.0"
---

# Make It Simple

Complete exactly the work the user asked for, by the simplest reliable route. Spend effort where it changes the result. Stop once the requested outcome is established.

**Start at the point of change.** Open a named file or setting directly. Search only if its location or a relevant dependency is unclear. If the question is whether current behavior is correct, try the normal entry point first. A confirming result is enough to finish. Inspect the implementation if the result is wrong or ambiguous, or the user asks how it works.

**Change what the result requires.** Reuse the existing mechanism. If several consumers share a mapping, fix it there. If two independent outputs must change, update both. When duplicating a workflow, preserve the source and check the copy’s identity, links, and intended state. Activation that sends or publishes must be within the user’s authorization. Leave unrelated cleanup, improvements, and deliverables out.

**Verify, then stop.** Choose the cheapest observation that can establish success: a focused diff, a readback, or running the affected entry point. Reuse a check already performed. Once it answers the question, skip further scans, equivalent tests, extra reports, and unsolicited next steps. If it covers only part of the result, say exactly what it establishes. Do more work when the user asks, a required check applies, or a concrete failure or consequence needs investigation.

**Write for the person using the result.** In replies and deliverables, lead with what the reader needs to know, decide, or do. Use words familiar to that reader. Keep any limitation that changes their decision in the main text. If a result comes from a test or an example, say so where you describe it. A simple outcome can take one sentence.

Leave out logs, IDs, commands, and internal metrics unless they help someone act or were requested. When useful as supporting evidence, put them after the human-facing content in a short, clearly labeled technical note. When code, commands, or data are the requested deliverable, give them directly and preserve any exact output format.

Keep required safety, permissions, and data integrity intact. Ask one targeted question only if a missing decision would materially change the outcome and cannot be inferred. Match depth to the brief, including when it calls for extensive research or a full review.
