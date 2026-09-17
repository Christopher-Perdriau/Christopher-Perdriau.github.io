---
title: "Projects"
permalink: /projects/
excerpt: "Applied software engineering work, for readers coming from an industry background."
---

Most of my public record is academic publications — this page is for readers who want evidence of applied, full-stack engineering work instead.

## Res-Intel Multifamily EUI Dashboard — Phase 1a

**Stack:** Svelte, Webpack, NestJS, AWS (Cognito, Secrets Manager)

Res-Intel's multifamily energy-use dashboard helps utility companies and property managers explore energy performance across thousands of properties. The team wanted to add an AI-assisted natural-language query feature, but the underlying dataset contained information that could not be exposed — directly or indirectly — to any external LLM service.

Rather than build the AI layer first, the team's feasibility plan called for a two-phase approach: ship a fully deterministic, client-side feature first, with zero LLM dependency, and layer natural-language routing on top of it later. This kept the feature useful and shippable independent of the AI work, and let the highest-risk data-exposure questions get worked out separately.

**What I built:** a summary-statistics feature that computes and displays aggregate metrics — property counts, energy-use averages, standard deviation, min/max ranges — for a set of properties, entirely client-side:

- `computeSummaryStats`, a pure function with no network dependency of its own, designed to work independently of the app's mapping library so the feature still functions if the map itself fails to load
- A collapsible stats-card UI component, placed to avoid an existing, fragile layout area in the sidebar that resized unpredictably with window size and filter state
- A non-LLM, client-side name/ID search component, satisfying the requirement that identifier lookups never pass through an AI model

**Beyond the feature code**, a meaningful part of this phase was reconstructing undocumented local-development infrastructure across two repositories and a third-party backend service: diagnosing a chain of failures across mismatched Node.js versions, a stale `.nvmrc`, and an HTTP/HTTPS protocol mismatch between services; tracing a misleading "Invalid Token" authentication error back through a guard clause to its actual root cause — missing local AWS credentials for a Cognito `AdminGetUser` call, silently swallowed several layers upstream; and identifying that the data source needed for aggregate statistics didn't yet exist in either accessible repository, then scoping the right question to ask the team member who owned that infrastructure rather than guessing at an undocumented service boundary.

Given the project's strict data-handling requirements, credential hygiene was part of the deliverable, not an afterthought: real secrets (API keys, database credentials, JWT secrets) were kept entirely outside both project directories, symlinked in only when actively testing and removed immediately after, and I set up OS-level sandboxing for AI-assisted coding tool use with explicit deny rules on credential files and directories — verified independently rather than assumed to work from configuration alone.

**Outcome:** Phase 1a shipped as a standalone, working feature — usable on its own, and ready to serve as the foundation for the natural-language query layer planned on top of it.

This project is a useful counterweight to an otherwise research-heavy CV: it shows full-stack engineering, architectural judgment (shipping a deterministic MVP before the riskier AI layer), and comfort working with cloud infrastructure.
