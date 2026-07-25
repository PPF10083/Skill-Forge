---
name: read-paper
description: Read and explain one academic paper through a quick relevance overview, deep reading, focused questions, explanations of key formulas, figures, and tables, associated code analysis, reference implementations, or Mermaid diagrams. Use only when the user explicitly invokes $read-paper or /read-paper.
---

# Read Paper

## Route the request

- With no requested mode, provide a quick overview and offer deep reading next.
- For a full or detailed explanation, use deep reading.
- For a focused question, including a formula, figure, or table, follow the focused-question guidance below.
- For code or diagram requests, follow the relevant section below.

## Scope

- Accept an attachment, pasted text, title, DOI, or URL. Find accessible paper or code material when needed.
- Handle one paper. If given several, ask the user to choose one.
- Use user background, goals, and selection criteria only when explicitly provided. Ask one concise question only when missing context blocks the requested relevance judgment.
- Use Chinese by default. Change languages only when explicitly requested, retaining important original terms when useful.
- Reply in the conversation unless the user requests a file.

## Evidence

- Base every substantive factual claim, explanation, and conclusion on the paper or clearly identified associated materials. When the available evidence is insufficient, state what is unknown or cannot be determined; never fill gaps with guesses or fabricated details.
- Locate important claims by page, section, table, figure, equation, appendix, or code position. State what was read when exact locations are unavailable.
- Distinguish author claims, explanations, and inferences. Separate author-stated limitations from inferred limitations.
- Preserve uncertainty, scope conditions, negative results, and qualifications. Never invent evidence or citations.

## Quick overview

Read the abstract and conclusion first; skip the introduction unless needed. Inspect methods, results, or key figures only as required. If only the abstract is available, proceed and disclose the limitation.

Keep the response to roughly 500 Chinese characters or a comparable length. Cover the paper's purpose, method, findings, and novelty; relevance to the user's stated needs or likely audience; gaps and risks; evidence locations, access limits, and the next useful step.

## Focused questions

- Answer only the requested question and inspect the surrounding context needed to answer it.
- For a formula, explain its purpose, notation, assumptions, intuition, and role in the method or conclusions.
- For a figure or table, explain how to read its structure, axes or fields, variables and comparisons, main result, and what the evidence does and does not establish.
- When asked for key formulas, figures, or tables without a specific target, select only those central to the method or conclusions.

## Deep reading

Require the full paper. If only an abstract or partial preview is available, ask for the full text.

Read all accessible sections. Begin with a summary of no more than 500 Chinese characters or a comparable length, covering contributions, methodological novelty, result significance, weaknesses, and future directions. Then explain:

1. Background and research question
2. Research method
3. Experimental or evidence design
4. Results and analysis
5. Conclusions, limitations, and future work

Adapt the structure for non-experimental papers. During deep reading, apply the focused-question guidance only to formulas, figures, and tables central to the method or conclusions. Do not repeat the opening summary.

## Associated code

- Prefer the official implementation and identify its source.
- Identify third-party reproduction code and its source. If no official implementation is available, generate pseudocode or a reference implementation only when useful. Mark all non-official code as non-author code; never present it as the author's implementation, assume it is reliable, or claim that it matches the original implementation.
- When inspecting a repository, explain its architecture and execution flow, map key elements to the paper, provide a minimal usage example, and cite code locations. Never invent repository APIs or behavior.

## Diagrams

- Create a Mermaid diagram when requested or materially useful.
- Choose a diagram type that clearly represents the relationships.
- Define the diagram's scope from the user's request and the paper.
- Inspect an author-provided figure before recreating it.
- Match the source figure's nodes and relationships.
- Preserve explicit start and end boundaries shown in the source figure.
- Preserve separate source panels as separate diagrams unless the user asks to combine them.
- Verify ambiguous figure labels against the caption and surrounding text.
- Keep explanatory additions outside the reproduced diagram.
- Compare the completed graph with the source figure before responding.
- Label a diagram without an author-provided figure as self-created.
