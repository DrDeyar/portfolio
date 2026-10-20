---
layout: post
title: "Phase 1 — Project Define: SFI Specification Search"
permalink: /csp/sprint-3/phase-1/define/
categories: [CSP, Project, Design-Thinking]
toc: true
---

## Phase 1 goal

The [Sprint 3 chart](https://pages.opencodingsociety.com/csp/sprint-3/) assigns **1 point** to “Project Phase: Define,” due in **Phase 1**. The course's [Design Thinking lesson](https://pages.opencodingsociety.com/agile/design_thinking) describes Define as a clear **problem statement**, **point of view**, and **user stories**.

This document defines a proposed improvement to the **SFI Foundation specification-search experience**. It is a planning artifact, not a claim that the improvement has been implemented or tested with users.

**Confirmed project:** SFI Foundation website. This definition uses the attached SFI Foundation frontend and backend repositories. Deyar confirmed this project for the Phase 1 assignment.

## Organization, audience, and evidence

**Organization:** SFI Foundation, Inc., a nonprofit that develops and administers standards for specialty/performance automotive and racing equipment. This description appears in the [archived official homepage in the frontend repository](https://github.com/SFI-Foundation/Frontend/blob/main/sfifoundation.com/index.html).

**Primary audience:** Racers and equipment buyers trying to locate an applicable SFI specification and its official source document.

**Secondary audience:** Team members, shops, and staff helping people navigate equipment information.

### What the repository establishes

- The [frontend README](https://github.com/SFI-Foundation/Frontend/blob/main/README.md) describes a prototype for browsing and searching SFI standards and PDF resources.
- The [current specs page](https://github.com/SFI-Foundation/Frontend/blob/main/navigation/sfi-specs.md) already includes search, category filters, results, and PDF links.
- The [existing Flask search handler](https://github.com/SFI-Foundation/Backend/blob/main/api/sfi_spec.py) accepts a `q` parameter and searches product names, spec numbers, categories, and subcategories.
- The shared [spec dataset](https://github.com/SFI-Foundation/Frontend/blob/main/_data/sfi_specs.json) contains structured product/category information and document references.

This is inherited project code. Its presence does **not** mean I wrote it, and existing search is not being presented as a new personal contribution.

### What still needs user research

The idea that users need clearer search explanations, predictable combined filters, and easier recovery from no results is a **design hypothesis**. No interviews, survey responses, client approval, or usability measurements have been supplied. Those must not be invented.

## Problem statement

Racers and equipment buyers need a clear way to narrow SFI specification records by an equipment description and category, understand why a result is relevant, and reach the official document, because a plausible-looking result alone does not explain whether it matches their specific question.

The existing prototype provides a starting point. The proposed work focuses on consistent filtering and understandable results rather than replacing the official standards or claiming to certify equipment.

## Point of view

**User:** A racer or equipment buyer who knows the equipment they are looking for but may not know its exact SFI specification number.

**Need:** Find relevant records, understand the match, and open the official source without guessing how search terms and category filters interact.

**Insight to validate:** Users may trust a search result more when the product name, spec number, category, and reason for the match are visible together. This is a hypothesis to check, not an interview finding.

**POV statement:** A racer unfamiliar with SFI numbering needs an understandable, predictable specification lookup because locating a document requires both useful search results and enough context to verify the source.

## User stories and acceptance conditions

| User story | Acceptance condition for later implementation |
| --- | --- |
| As a racer, I want to search by an equipment name or spec number so I can find relevant records. | Leading/trailing spaces and letter case do not change equivalent searches. Each returned record shows the product, spec number, and category. |
| As a buyer, I want my selected category and search text to work together so unrelated categories do not appear. | Every returned record matches the selected category, unless “All” is selected, and satisfies the defined text-matching rule. |
| As a new user, I want to know why a record matched so I can check its relevance. | Results identify matched terms or fields using a concise explanation. A match is not labeled a certification or safety determination. |
| As a user with no matching results, I want a clear next action so I can recover. | A zero-result state preserves my input and offers clearing the search or selecting “All.” A network error has a different message. |
| As a user reviewing a standard, I want an official source link so I can verify the document myself. | Available document links are shown; missing links are labeled unavailable and are not replaced by invented URLs. |

## Scope and boundaries

**Proposed personal feature:** Improve the specification search/filter flow from frontend input through backend processing to an explained result list. Deyar is the proposed owner of this bounded feature, subject to team agreement.

The feature definition includes query normalization, combined text/category rules, result explanations, and empty/error states. The exact interface design and algorithm alternatives belong to the later Ideate phase.

Out of scope for this feature are payments, official certification decisions, a replacement for SFI testing, a new authentication system, image recognition, a chatbot, and automatic PDF summarization. Existing project features remain inherited work.

## Input, processing, output, and data

| Area | Definition |
| --- | --- |
| Input | User-entered query text and a selected category. |
| Source data | Existing SFI specification records: product name, spec number, category, subcategory, and source-document references. |
| Processing contract | Normalize text; apply a documented text-matching rule and the chosen category together; collect relevant records and explanations. |
| Output | A result list with identifying fields and source links, or a clear no-result/error message. |
| Data boundary | Public specification data is sufficient for search; personal user profiles and gear records are unnecessary for this feature. |
| Responsibility boundary | The tool helps locate documents. Users must consult current official requirements; search matches do not establish equipment compliance. |

## CPT preparation map — planned evidence

The course asks students to connect their own feature to the Create Performance Task. This table is a **plan**, not completed CPT evidence or a claim of authorship over the starter code.

| Requirement | Proposed evidence to develop later |
| --- | --- |
| Purpose | Help a racer locate and understand relevant specification records. |
| Input/output | A query and category produce explained results or a meaningful empty state. |
| Collection | A list of specification records processed together. Without it, separate hard-coded checks and output blocks would be needed for individual records. |
| Student-developed procedure | A proposed `find_matching_specs(specs, query, category)` procedure whose query and category parameters affect the returned results. Deyar must develop, understand, and explain the eventual code. |
| Sequencing | Normalize inputs before evaluating records and constructing results. |
| Selection | Decide whether a record satisfies the matching and category conditions. |
| Iteration | Examine the records in the collection. Sequencing, selection, and iteration must occur together inside the selected procedure. |
| Procedure call | The search handler passes records and validated input to the procedure and uses its return value in the response. |
| Testing | Compare expected and actual behavior for the cases below after implementation. |

Framework calls, database queries, and copied starter logic alone do not establish a student-developed procedure. Follow the course's linked official rules for attribution and independently prepared video/PPR materials.

## Proposed validation cases

These are expected outcomes for later work, **not tests already run against a new feature**.

| Case | Expected behavior |
| --- | --- |
| `helmet` and `  HELMET  `, same category | Equivalent record sets after normalization. |
| Equipment query with a specific category | All returned records satisfy both conditions; no unrelated-category records leak through. |
| A term absent from the dataset | Empty results with a recovery action, rather than an exception or misleading match. |
| Blank query with a category | Browse that category using an explicitly documented empty-query rule. The existing search endpoint currently rejects a blank query; any change needs a deliberate API contract. |
| A record lacking a PDF reference | Display the record and explain that the document link is unavailable. |
| Backend unavailable | Show a connection error separately from “no specs match.” |

## Team handoff and open decisions

Before the team adopts this Define document:

- Review and approve the bounded personal feature within the confirmed SFI Foundation website project.
- Confirm the actual team members and their roles; no names or role assignments are assumed here.
- Record the agreed problem, owner, and acceptance conditions in the team's planning Issue and board. This document does not claim those remote artifacts have been created.
- Validate the user need through a real conversation or observed task, recording actual feedback and revising the problem statement if needed.

The next phase is to compare solution ideas against this definition. This Phase 1 artifact does not complete Ideate, Prototype, or Test assignments.

## Sources and preparation note

- [Sprint 3 chart, project goals, and CPT preparation](https://pages.opencodingsociety.com/csp/sprint-3/)
- [Define: problem statement, POV, and user stories](https://pages.opencodingsociety.com/agile/design_thinking)
- [Frontend](https://github.com/SFI-Foundation/Frontend) and [Backend](https://github.com/SFI-Foundation/Backend) source repositories

Prepared with AI assistance from course guidance and the attached repositories. Deyar and the team must review project scope, ownership, and any personal claims before submission.
