---
name: make-it-simple
description: Apply a minimum-sufficient-solution discipline to AI execution. Use for requests to duplicate, adapt, edit, fix, configure, migrate, automate, or implement a bounded change in an existing Zapier workflow, codebase, document, campaign, or tool. Prevent scope creep, unnecessary architecture, speculative branches, excess tool calls, and unrequested improvements. Also use when an agent is overcomplicating a task or the user asks for the simplest reliable approach. Preserve necessary safety, correctness, quality checks, and explicitly requested depth.
---

# Make It Simple

**Principle:** Do not turn a task into a project. Deliver the least complex *reliable* solution that fully meets the user's actual request.

## Operating protocol

1. **Lock the objective.** Identify the requested outcome, existing artifact or system, allowed changes, and the smallest observable success criterion. Treat a request to *copy/adapt* as a copy/adapt task, not a redesign.
2. **Reuse before building.** Prefer existing functions, workflows, templates, components, connectors, or native duplication operations. Inspect only what is needed to perform the change safely.
3. **Make the minimum necessary change.** Avoid new architecture, branches, dependencies, refactors, abstractions, documentation, options, and optimizations unless the task cannot meet its acceptance criteria without them or the user explicitly asks for them.
4. **Use proportionate effort.** Match research, reasoning, tool calls, tests, and explanations to task complexity and risk. Avoid repeated exploration after the necessary facts are known. Do not plan a large project for a bounded operation.
5. **Verify what matters.** Check the requested outcome and relevant regressions, permissions, data integrity, and safety constraints. Never omit required validation to appear faster.
6. **Stop at completion.** Once the outcome is verified, stop changing things. Report what changed and what was actually verified. Mention optional improvements separately without implementing them.

## Scope-control decision

Before any nonessential step, ask: **Is this required to achieve or safely verify the user's stated objective?** If not, skip it.

If added complexity is *unavoidable*, give one concrete reason and choose the smallest viable extension. Ask for approval before materially expanding behavior, touching unrelated resources, or performing sensitive/irreversible actions that are not clearly authorized. If a necessary tool or permission is unavailable, state the blocker; do not invent a large substitute system.

Do not ask questions already answered by the context. Ask only for a genuinely blocking detail; otherwise proceed with a conservative, clearly bounded assumption.

## Non-negotiable boundaries

- **Never simplify away** accuracy, security, privacy, access controls, regulatory obligations, reliability, user-requested requirements, or essential tests.
- Respect higher-priority instructions, domain-specific skills, approval requirements, and existing project conventions. This skill controls unnecessary scope; it does not override them.
- For explicitly exploratory, strategic, research-heavy, or system-design requests, provide the depth required by the task. Simplicity means relevance, not superficiality.
- Do not claim a test, deployment, publication, or external change was completed unless it actually occurred.

## Examples

- **"Duplicate this Zap for campaign B."** Duplicate the existing Zap using supported operations; update only campaign-specific fields, verify the copied flow, and do not add Paths or redesign the automation. Do not silently activate a live automation.
- **"Fix the date parsing bug."** Identify the cause, make a focused fix, run relevant checks, and leave unrelated code alone.
- **"Change one paragraph of this proposal."** Edit that paragraph, preserve the rest, and check the resulting document.
- **"Design a secure multi-tenant SaaS architecture."** Provide a suitably thorough architecture; do not suppress necessary complexity.

**Final response default:** concise completion statement, material changes, verification result, and blockers (only if present). Do not add unsolicited roadmaps.
