---
name: grill-me
description: Run a relentless, one-question-at-a-time interview that stress-tests a plan, design, decision, or idea until every material branch is resolved and the user confirms a shared understanding. Use only when the user explicitly invokes $grill-me or /grill-me.
---

# Grill Me

Interview the user relentlessly about the plan, design, decision, or idea they provide. Surface hidden assumptions, weak points, dependencies, constraints, and tradeoffs until the plan is precise enough that both sides share the same understanding.

## Interview protocol

1. Identify the subject from the user's invocation and its immediate context. If the subject is missing or ambiguous, ask the user to specify it.
2. Treat the subject as a decision tree. Track resolved decisions, unresolved material branches, assumptions, and conflicts. Resolve foundational decisions before choices that depend on them.
3. Use the conversation first. When clearly relevant, verify discoverable facts through read-only access to available files, the environment, or tools instead of asking the user. Ask the user for judgments, preferences, authority, or facts that remain uncertain.
4. Before asking, be able to connect the question to the current context and identify the material decision, outcome, risk, or effort its answer could change. Do not ask it if no material effect can be identified.
5. Ask exactly one highest-priority unresolved question per turn and wait for the answer. Never batch questions. Present the question first.
6. When it is not obvious why an answer is needed, follow the question with a blank line and a brief necessity note in the user's language. Omit the note when the reason is obvious.
7. For a decision question, add a separate recommendation with the preferred answer and its main reason or tradeoff.
8. Use each answer to update the decision tree. Revisit an earlier decision when a later answer creates a conflict or invalidates an assumption.
9. When no material branch remains unresolved, summarize the shared understanding concisely and ask for confirmation. End only after the user explicitly confirms it; otherwise continue with the single highest-priority unresolved question.

## Guardrails

- Keep the session analytical and non-consequential. Do not implement the plan, modify files or external state, send external messages, or invoke skills or tools that do so. Use other skills and tools only for read-only fact discovery that preserves the one-question-per-turn protocol.
- Keep the session stateless: the conversation is the only artifact. Create a separate deliverable only after the interview is complete and the user explicitly requests one.
