---
name: explain
description: Explain terms, concepts, mechanisms, and established methods or systems at a depth suited to the user. Use only when the user explicitly invokes $explain or /explain. Do not use to design, review, or execute a custom solution.
---

# Explain

## Interpret the request

1. Identify the target. Treat a standalone term as an explanation request, but not as evidence for a particular meaning.
2. Infer the user's apparent knowledge level from their wording, questions, and established context.
3. Determine the intended meaning before explaining:
   - If the request or context clearly supports one interpretation, use it.
   - If multiple meanings remain plausible, ask one concise clarifying question and stop. Do not guess or begin the explanation.
   - If no reliable meaning can be identified, ask for the source or surrounding context.

## Build the explanation

1. State what the target is first, then adapt the explanation:
   - When foundations appear limited, use plain language, explain only necessary terminology, and give an intuitive example.
   - When the user already shows understanding, increase the technical depth directly; do not force an analogy or example.
2. Add only the purpose, cause, mechanism, or prerequisite needed for a correct understanding. Define a necessary prerequisite in one sentence where it becomes relevant, then return to the target.
3. For a broad concept, establish its core definition and minimal framework without turning the response into a complete textbook treatment.
4. Include formulas, code, or formal notation when accurate understanding requires them, the user requests them, or the user demonstrates the relevant background. Explain each included element.
5. When several related terms are requested, state their common ground first, then highlight the decisive differences and when each applies.

## Protect accuracy

- Correct material misunderstandings explicitly and briefly.
- Use an analogy only when it preserves the concept's core relationship. State its key limitation when it could create a misleading mental model.
- Raise at most one common misconception, and only when it would materially change the user's understanding.
- When definitions differ materially, explain their shared core first, then only the differences that affect interpretation.
- State a concept's boundary directly when its name may invite a conclusion beyond what it actually means; avoid generic disclaimers.

## Use evidence and source context

- Verify and cite reliable sources when the concept is recent, changeable, disputed, uncertain, or the user asks for sources.
- When the target appears in a paper or other large source, read only the passages needed to explain it. Do not expand the task into an analysis of the full material.

## Deliver naturally

- Use Chinese for the user-facing explanation unless the user requests another language. Include an original term, foreign-language full name, or abbreviation once when it improves understanding, resolves ambiguity, or supports later lookup.
- Organize the explanation naturally instead of forcing fixed headings or a rigid response template.
- On a later explicit invocation in the same conversation, build on the understanding already established. Do not restart the explanation from first principles unless the user asks or the prior foundation is no longer adequate.
- Make the response self-contained for the current request without appending a routine offer to explain more.
